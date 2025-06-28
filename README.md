# ATS-Friendly-Resume-Builder-with-score-checker

This application provides a user-friendly interface to build your resume. As you fill in the details in the left pane, the right pane will show a live preview of how your resume will look. You can add multiple education and experience entries dynamically.

Here's how to use it:

Fill in Details: Use the form fields under "About You", "Education", and "Experience" to enter your information.

Add Sections: Click "+ Add Education" or "+ Add Experience" to add more entries for these sections.

Live Preview: Observe the "Live Resume Preview" on the right side as you type.

Export as PDF: Click the "Export as PDF" button to download your resume as a PDF document.

Generate QR Code: Click the "Generate QR Code" button to create a QR code that, when scanned, will display your resume data in JSON format.

Key Changes:
ATS Score Checker Section:

A new ATS Score Checker section has been added to the left (form) column.

It includes a textarea for you to paste the job description or relevant keywords.

A ATS Score: --/100 display and an ATS Feedback area provide real-time analysis.

ATS Score Logic (calculateAtsScore function):

This new JavaScript function performs a basic ATS analysis:

Keyword Matching: It extracts keywords from your provided job description/keywords, normalizes them, and checks for their presence in your resume content. It gives a score based on the proportion of matched keywords.

Section Presence: Awards points for having Professional Summary, Education, and Experience sections.

Bullet Point Usage: Encourages the use of bullet points in the Experience section.

Resume Length: A very basic check to ensure the resume is not too short or too long.

Feedback Messages: Provides suggestions on how to improve your ATS score (e.g., missing keywords, suggestions for sections, bullet points).

The calculateAtsScore function is called every time you type in the resume fields or the job description input, providing real-time feedback.

ATS-Friendly Formatting Considerations:

The existing resume preview is already designed with clarity and standard formatting, which inherently makes it more ATS-friendly (e.g., clear headings, standard sections, good readability).

The new ATS section provides explicit guidance to the user on this.

Now you can paste a job description or key terms into the ATS checker, and the builder will give you an immediate assessment of how well your resume is optimized for those terms, along with suggestions for improvement!
