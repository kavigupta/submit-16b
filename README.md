# Submit-16B

Submitting EE assignments through `ssh` and `glookup` can often be tedious. However, there is an easier way: `submit-16b`. In one command, `submit-16b` does the following:

 - Checks to see if the appropriate files exist
 - Converts the `.ipynb` to a `.pdf` and tacks it onto the end of the existing `.pdf` (if applicable)
 - Copies the submission files to the server, and places them in a folder
 - `submit`s the files on the server
 - Calls `glookup -t` so you can check that the assignment was in fact submitted
 - Resets everything on your computer back to how it was, saving the submission pdf as `-final-submission.pdf` if it was modified

You can check the result of the merging process by looking at the `-final-submission.pdf`. `submit-16b` is your one-stop shop for submitting EE16A and EE16B assignments!

# Usage Examples

`submit-16b` has a fairly simple interface. To submit a Homework 9, run

```sh
./submit-16b hw 9
```

in the folder containing the files for submission (which must have the names `hw9.pdf` and `prob9.ipynb` or `hw9.ipynb`).

To submit the self-grade for homework 9, run

```sh
./submit-16b grades 9
```

in the folder containing the file `hw9_grades.txt`.

The first time you run `submit-16b` you will be prompted for information regarding your server. However, this is stored and you won't be asked for it again. You will, however, be asked to confirm files to submit every time, this makes sure you know what is being submitted.

If you would like to submit to a different server, run

```sh
./submit-16b clean
./submit-16b hw 9
```

# Bug Reports

If you encounter a bug with this software, please email me at my Berkeley email (`kavi` at Berkeley) or file an issue on Github.

# License

(Ever wondered why the BSD License is always in shouty-case? Never understood it myself.)

THIS SOFTWARE IS PROVIDED BY KAVI GUPTA AS IS AND WITHOUT ANY WARRANTIES. IN NO EVENT SHALL KAVI GUPTA BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
