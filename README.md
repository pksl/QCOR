# QCOR(Query-Customized Online Reason System)

## Experiment Setup

All tests were run on an Intel(R) Xeon(R) CPU E5-4603 2.00GHz machine with 100GB heap size for the Java VM under the CentOS Linux release 7.9.2009 (Core).



## UOBM SPARQL

```
# queries expressed in SPARQL
# [query ID]
# query

^[query1]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:UndergraduateStudent . 
 ?x benchmark:takesCourse <http://www.Department0.University0.edu/Course0>
}

^[query2]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Employee 
}

^[query3]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Student . 
 ?x benchmark:isMemberOf <http://www.Department0.University0.edu>
}

^[query4]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Publication . 
 ?x benchmark:publicationAuthor ?y .
 ?y rdf:type benchmark:Faculty . 
 ?y benchmark:isMemberOf <http://www.Department0.University0.edu>
}

^[query5]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:ResearchGroup . 
 ?x benchmark:subOrganizationOf <http://www.University0.edu>
}

^[query6]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Person . 
 <http://www.University0.edu> benchmark:hasAlumnus ?x 
}

^[query7]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Person . 
 ?x benchmark:hasSameHomeTownWith <http://www.Department0.University0.edu/FullProfessor0>
}

^[query8]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:SportsLover . 
 <http://www.Department0.University0.edu> benchmark:hasMember ?x
}

^[query9]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:GraduateCourse . 
 ?x benchmark:isTaughtBy ?y .
 ?y rdf:type benchmark:SportsLover . 
 ?y benchmark:isMemberOf ?z .
 ?z benchmark:subOrganizationOf <http://www.University0.edu>
}

^[query10]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x benchmark:isFriendOf <http://www.Department0.University0.edu/FullProfessor0>
}

^[query11]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Person . 
 ?x benchmark:like ?y . 
 ?z rdf:type benchmark:Chair .
 ?z benchmark:isHeadOf <http://www.Department0.University0.edu> . 
 ?z benchmark:like ?y
}

^[query12]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Student . 
 ?x benchmark:takesCourse ?y .
 ?y benchmark:isTaughtBy <http://www.Department0.University0.edu/FullProfessor0>
}

^[query13]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:PeopleWithHobby . 
 ?x benchmark:isMemberOf <http://www.Department0.University0.edu>
}

^[query14]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:Woman . 
 ?x rdf:type benchmark:Student . 
 ?x benchmark:isMemberOf ?y . 
 ?y benchmark:subOrganizationOf <http://www.University0.edu>
}

^[query15]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:PeopleWithManyHobbies .
 ?x benchmark:isMemberOf <http://www.Department0.University0.edu>
}

^[query16]
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX benchmark: <http://semantics.crl.ibm.com/univ-bench-dl.owl#>
SELECT ?x
WHERE {
 ?x rdf:type benchmark:WomanCollege .
}
```

