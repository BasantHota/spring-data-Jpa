# spring-data-Jpa
How to work on Spring data Jpa

What is Spring Data JPA?
It is a library / framework that adds an extra layer of abstraction on the top of our JPA provider
If we decide to use Spring Data JPA, the repository layer of our application contains three layers that are described like below
 
1.Spring Data JPA 
provides support for creating JPA repositories by extending the Spring Data repository interfaces.
2.Spring Data Commons 
provides the infrastructure that is shared by the data store specific Spring Data projects
3.JPA Provider-implements the Java Persistence API

## code changes for latest spring boot version

    @GetMapping
    public Page<Employee> getEmployees() {
        return repository.findAll(PageRequest.of(0, 3));
    }

    @GetMapping("sort/{field}")
    public List<Employee> sortEmployeeByField(@PathVariable String field) {
        return repository.findAll(Sort.by(field));
    }
