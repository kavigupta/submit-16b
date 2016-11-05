# Submit-16B

Submitting EE assignments through `ssh` and `glookup` can often be tedious. However, there is an easier way. `submit-16b` is a simpler way to submit documents. In one command, `submit-16b` does the following:

 - Checks to see if the appropriate files exist
 - Converts the `.ipynb` to a `.pdf` and tacks it onto the end of the existing `.pdf`
 - Copies the `.pdf` and `.ipynb` files to the server, and places them in a folder
 - `submit`s the files on the server
 - Calls `glookup -t` so you can check that the assignment was in fact submitted

You can check the result of the merging process by looking at the `-final-submission.pdf`

# Usage Examples

`submit-16b` has a fairly simple interface. To submit a Homework 9, run

```
./submit-16b hw 9
```

in the folder containing the files for submission (which must have the names `hw9.pdf` and `prob9.ipynb` or `hw9.ipynb`).

To submit the self-grade for homework 9, run

```
./submit-16b grades 9
```

in the folder containing the file `hw9_grades.txt`.

The first time you run `submit-16b` you will be prompted for information regarding your server. However, this is stored and you won't be asked for it again. You will, however, be asked to confirm files to submit every time, this makes sure you know what is being submitted.

# Bug Reports

If you encounter a bug with this software, please email me at my Berkeley email (`kavi` at Berkeley) or file an issue on Github.