# University Course Schema Design 
 
## Summary 
We're going to design a database schema that would support a university course enrollment application.  Imagine an application where students are able to browse the university's course offerings.  Each of the university's courses is listed.  Students browse the list and enroll in courses.  The specific requirements are presented in the releases.


## Releases
### Release 0: Basic Schema
Begin by designing a database schema based on the requirements listed below.  Use [Schema Designer][] to visually represent your schema.

- A student can enroll in many courses.
- A course can have many enrolled students.
- A student receives a final grade for each enrolled-in course (think carefully about what table this data lives in).
- A course is taught by one teacher.
- A teacher can teach multiple courses.


###Release 1 : Updated requirements

New requirements!  These replace the ones above.

1. Classes have many sections
2. Sections have a start time and an end time
3. Sections can either be Monday/Wednesday/Friday or Tuesday/Thursday
4. Students can attend many classes and must be assigned to a specific section,
   but they can only attend one section per class
5. Students are given a grade per section
6. Teachers can teach multiple sections, but a section is taught by only one teacher
7. Classes belong to a single department, but a department has multiple classes

Design an advanced "course database" using the requirements above.

###Release 2 : Enforcing time constraints

How would you enforce time constraints?  For example, students can't attend and teachers can't teach two sections whose times overlap.

With your pair, talk about how you'd do this.  Hint: you might want to use a whiteboard.

Are you able to infer if student and teacher data violate this constraint?  Even if the database itself doesn't have this constraint built in, if you can infer a violation, you could conceivably write ruby code to ensure this violation doesn't occur.  

What are the potential costs if you are relying on supporting ruby code to help validate your data?  Write an explanation in your gist.

#### Cross-listing classes

Sometimes schools allow courses to be cross-listed in multiple departments.  For example, a Combinatorics class might be in both the Mathematics and Computer Science departments.  

How would you alter the schema above to accommodate that?

When you are done, take a screenshot of your final schema design, and commit it.

<!-- ##Optimize Your Learning  -->

## Conclusion

[Schema Designer]: https://schemadesigner.devbootcamp.com/
