Issue #1: Form Submit Button Outside the Form

The issue, why this is an issue, and the solution:

The submit and reset buttons are located outside of the <form> element. Because they are not contained within the form, the submit button will not
submit the form data and the reset button will not reset the form fields. This breaks the expected functionality of HTML forms and can confuse users.

Initial code:

</form>

<div
  class="form space-evenly-distributed-row-container form-buttons-container"
>
  <input class="form-button" type="submit" value="submit" />
  <input class="form-button" type="reset" value="reset" />
</div>

Updated code:

<div
  class="form space-evenly-distributed-row-container form-buttons-container"
>
  <input class="form-button" type="submit" value="Submit" />
  <input class="form-button" type="reset" value="Reset" />
</div>
</form>

Issue #2: Form Labels Are Not Properly Associated With Inputs

The issue, why this is an issue, and the solution:

Several form fields use <span> elements as labels instead of proper <label> elements. While the text appears visually correct, screen readers cannot
properly associate the text with the input field. Additionally, users cannot click on the text label to focus the corresponding input. This is an
accessibility and semantic HTML issue.

Initial code:

<p class="label-input-group form-element-container">
  <span class="form-label">Name</span>
  <input
    aria-label="name"
    class="form-input-box"
    type="text"
    id="name"
    name="name"
  />
</p>

Updated code:

<p class="label-input-group form-element-container">
  <label class="form-label" for="name">Name</label>
  <input
    class="form-input-box"
    type="text"
    id="name"
    name="name"
  />
</p>
