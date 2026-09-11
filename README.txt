SBT-DF203 — Lab 3: SYN Flood Attack Investigation Using TShark
Student: Mary-Joy Adewole | Reg No: 2025/FWSD/11468
Package prepared: 11 September 2026

============================================================
WHAT'S IN THIS PACKAGE
============================================================

SBT-DF203-Lab3_2025-FWSD-11468_Mary-Joy-Adewole.pdf
    Final forensic report — required submission format/filename per
    the lab manual. Contains all 13 evidence screenshots, the
    chain-of-custody worksheet, quantitative findings, the
    normal-vs-suspicious comparison table, and the full command
    appendix.

SBT-DF203-Lab3_2025-FWSD-11468_Mary-Joy-Adewole.docx
    Editable Word version of the same report.

screenshots/ (13 files)
    Original, full-resolution terminal screenshots, numbered
    Screenshot__310_.png through Screenshot__322_.png. Same images
    appear (resized) in the report as Figures 1-13 - see the Figure
    Index in the report's Appendix for which screenshot maps to
    which figure and checklist item.

reports/ (10 files: .txt / .tsv)
    Command output records - hashes, handshake field extractions,
    SYN/SYN-ACK/RST lists, counts, unique ports, expert-info.
    ACTION NEEDED: replace these with your real files - see Step 1.

scripts/syn_probe_lab.py
    The bounded 4-packet Scapy simulation script exactly as
    specified in the manual (TARGET=127.0.0.1, PORT=80, COUNT=4).

evidence/  and  working/
    Placeholder folders for your original PCAP/PCAPNG files -
    currently empty. ACTION NEEDED - see Step 1.

============================================================
STEP 1 - REPLACE PLACEHOLDER FILES WITH YOUR REAL ONES
============================================================

The report and this README were built from your terminal
screenshots, not from direct access to your Kali VM. Two sets of
files here are stand-ins for the real thing and MUST be swapped
before you submit or push to GitHub:

  1. evidence/ and working/ are EMPTY. Your actual capture files
     belong here:
       evidence/mySYNFloodCapture.pcap
       evidence/normal_http.pcapng
       evidence/bounded_syn_activity.pcapng
       working/bounded_syn_activity_working.pcapng

  2. reports/*.txt and reports/*.tsv in this package are TYPED
     TRANSCRIPTS of what's visible in your screenshots. Your VM has
     the real command-output files at the same paths - overwrite
     the ones in this package with those.

On your Kali VM, from inside ~/SBT-DF203-Lab3, run:

    cp evidence/mySYNFloodCapture.pcap evidence/normal_http.pcapng \
       evidence/bounded_syn_activity.pcapng \
       working/bounded_syn_activity_working.pcapng \
       reports/*.txt reports/*.tsv \
       scripts/syn_probe_lab.py \
       /mnt/hgfs/<your-shared-folder-name>/SBT-DF203-Lab3/

(If /mnt/hgfs isn't mounted: sudo mkdir -p /mnt/hgfs && sudo
vmhgfs-fuse .host:/ /mnt/hgfs -o allow_other - or enable shared
folders under VM Settings -> Options -> Shared Folders in VMware.)

Then, on Windows, copy the files that land in your shared folder
into this package, overwriting the matching placeholders:
  - the 4 pcap/pcapng files -> into evidence/ and working/ here
  - the 9 .txt/.tsv files    -> overwrite reports/ here
  - syn_probe_lab.py         -> overwrite scripts/ here (should be
                                 identical, just confirms integrity)

============================================================
STEP 2 - TWO DIFFERENT USES FOR THIS FOLDER
============================================================

A) PORTAL / ZIP SUBMISSION
   Zip this whole folder, named with your registration number and
   lab number:
       2025-FWSD-11468_SBT-DF203-Lab3.zip
   Submit that zip as required by the assessment portal.

B) GITHUB UPLOAD (your usual workflow)
   Do NOT upload the zip file to GitHub. Upload the CONTENTS of this
   folder (the .pdf, .docx, README.txt, and the evidence/, working/,
   reports/, screenshots/, scripts/ folders) directly, unzipped, via
   GitHub's web upload. Full step-by-step is in the chat reply that
   came with this file.

============================================================
SUBMISSION NAMING (per manual "Submission Requirements")
============================================================
- Report PDF: SBT-DF203-Lab3_RegNo_FullName.pdf -> already correct.
- Final ZIP (portal): name with reg number + lab number, e.g.
  2025-FWSD-11468_SBT-DF203-Lab3.zip

============================================================
ACADEMIC INTEGRITY
============================================================
All commands, screenshots, observations and conclusions in this
package are the student's own work, produced during an individual
authorized practical assessment, per the Academic Integrity and
Authorization Statement in the SBT-DF203 Lab 3 manual.
