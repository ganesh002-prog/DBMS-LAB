# DBMS LAB

Database Management Systems lab record for Experiments 1–10, based on the supplied **DBMS LAB.docx** manual.

Each experiment has two files:

- `README.md`: Aim, Program, and Result.
- `output.md`: expected output only, separated from the program.

| Experiment | Aim, program and result | Output |
| --- | --- | --- |
| EXP1 | [Database creation and information retrieval](EXP1/README.md) | [Output](EXP1/output.md) |
| EXP2 | [Insertion, deletion, updating, altering and viewing records](EXP2/README.md) | [Output](EXP2/output.md) |
| EXP3 | [DCL and TCL commands](EXP3/README.md) | [Output](EXP3/output.md) |
| EXP4 | [SQL constraints](EXP4/README.md) | [Output](EXP4/output.md) |
| EXP5 | [ANY, ALL, IN, EXISTS and set operations](EXP5/README.md) | [Output](EXP5/output.md) |
| EXP6 | [Aggregate functions, GROUP BY and HAVING](EXP6/README.md) | [Output](EXP6/output.md) |
| EXP7 | [Views, sequences, indexes and savepoints](EXP7/README.md) | [Output](EXP7/output.md) |
| EXP8 | [Normalization from 1NF to 5NF](EXP8/README.md) | [Output](EXP8/output.md) |
| EXP9 | [Relationships, joins and subqueries](EXP9/README.md) | [Output](EXP9/output.md) |
| EXP10 | [PL/SQL programming](EXP10/README.md) | [Output](EXP10/output.md) |

## Environments

Experiments 1–6 and 9 use MySQL 8.0.31 or later. Experiments 7, 8, and 10 use Oracle Database; Experiment 10 requires Oracle 12c or later for its identity column. Use SQL*Plus or SQL Developer script mode for PL/SQL.

Each MySQL experiment uses its own `DBMS_EXP<number>` database. Run each experiment once with no existing tables of the same names. Use a separate fresh Oracle lab schema for each Oracle experiment to avoid conflicting table names. Experiment 3 assumes the lab accounts `user1` and `student1` already exist and that the executing account can manage their table privileges. Constraint and exception demonstrations intentionally raise errors; run them individually and continue afterward.

## Output notes

Output files contain expected query rows, status messages, and errors derived from the supplied programs and sample data. They are not transcripts of MySQL or Oracle execution. Relational query results were cross-checked in an in-memory SQLite database, with dialect-specific operations handled separately. DCL, Oracle sequences, PL/SQL, and native DBMS behavior still require execution in the stated environment. Error wording, row order without ORDER BY, numeric formatting, audit timestamps, and generated constraint names may vary.

The source examples were organized and corrected where necessary:

- Widened the gender column to fit its `Not Specified` default.
- Kept MySQL-compatible ALTER syntax and removed a stray punctuation mark from a HAVING query.
- Committed the Book baseline before demonstrating transactions; its final full rollback restores the original prices.
- Corrected Experiment 9’s above-average-CGPA output to match the sample data.
- Added the missing PL/SQL execution delimiter and enabled server output. Kept one salary-increase invocation; the two source invocation forms are alternatives.
- Disabled the weekend trigger after its definition so the later cursor demonstration can run on any day.

The manual’s contents page also lists a mini-project item, but the supplied detailed material and this record cover the requested ten experiments. Unanswered practice questions are not treated as additional programs.

## Source

Adapted from the supplied Database Management System Lab Manual prepared by J. Hemapoorani, Department of Computer Science and Engineering, SCSVMV University.

- [MySQL set operations](https://dev.mysql.com/doc/refman/8.0/en/set-operations.html)
- [Oracle SQL*Plus documentation](https://docs.oracle.com/en/database/oracle/oracle-database/21/sqpug/)
