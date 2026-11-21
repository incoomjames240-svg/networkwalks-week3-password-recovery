NetworkWalks Week 3 Password Recovery Portfolio

James Kwabena Incoom

This portfolio records an authorized cybersecurity training exercise using the PDF files supplied for the NetworkWalks Week 3 labs.

Objective
Recover passwords for protected training PDFs, verify the results by opening the files, and document the tools, evidence, and lessons learned.

Module 1: John the Ripper through Johnny
I configured Johnny to use the John the Ripper executable, extracted the PDF password hash, saved the extracted hash in a text file, and loaded that file into Johnny. Johnny recovered good-luck for My Locked PDF1.pdf. I verified the result by opening the PDF. The report contains the Johnny result screenshot.

Module 2: NetworkWalks tools
I used the extracted PDF password hash with the NetworkWalks Password Cracker. The built-in list did not find PDF1's password. For My Locked PDF2.pdf, the built-in list found password1 at candidate 91 of 100. I verified the password by opening PDF2, which displayed the red unlocked padlock image.

Scope note
The supplied Module 2 task sheet names PDF1. The successful browser-tool evidence here is for PDF2. The PDF1 built-in-list failure is included as an observed result; it is not presented as a successful recovery with that list.

Troubleshooting and learning
A file checksum such as MD5 or SHA-256 identifies file contents. An extracted PDF password hash contains the information needed to test password candidates. A wordlist contains candidate passwords, one per line.

Uploading the hash text file as a wordlist tested the hash string as a candidate password and returned no match. Selecting a real password list corrected that input mistake. Loading a raw PDF as a password-hash text file in Johnny also produced incorrect entries; the extracted hash text file was the appropriate input.

Original PNG evidence
The screenshots below are the original uploaded PNG files, without resizing, redrawing, or conversion.

Screenshot 2026-11-20 224110.png — PDF1 opened successfully.
Screenshot 2026-11-20 225921.png — PDF1 returned no match with the browser tool's built-in list.
Screenshot 2026-11-20 231628.png — PDF3 opened and displayed a flag. Its recovery method is not documented here.
Screenshot 2026-11-21 134331.png — PDF2 opened and displayed the red unlocked padlock.
Screenshot 2026-11-21 135154.png — Browser tool recovered password1 for PDF2.

Report
James_Incoom_Week3_Password_Recovery_Portfolio.pdf contains the write-up and supporting images, including the Johnny result.

Lessons
Dictionary attacks succeed when the correct password is included among the tested candidates. A no-match result means that the tested list did not contain a matching candidate. It does not prove the PDF cannot be opened. Correctly distinguishing the protected file, extracted hash, and wordlist is essential.
