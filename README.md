# Availity
Mirth Interview Project for Availity
HL7 Gateway Programming Exercise
The files for this project reside online at the following link as a backup:
https://www.mediafire.com/folder/27naidd77scsq/Availity

In that link is the Availity.zip file. You will find the following:
• Availity Homework – Mirth HL7.pdf
o Answers to questions and project description
• 5csv.zip
o the csv files that Component #1 will ingest.
• HL7 Consumer Mirth v4_5_1.xml
• HL7 Producer Mirth v4_5_1.xml

The project consists of 2 Channels:
Channel 1: HL7 Producer - Component #1. This channel will ingest 5 delimited files from the "in"
folder, and create 1 HL7 message from each row of data. The result will be 5 HL7 files written to
the "out" folder. Messages will have a message header (MSH), patient demographics (PID), and
visit information (PV1). It will also include an additional NK1 segment. This channel will then send
both the HL7 and the channel name to Channel #2 named "HL7 Consumer".

Channel 2: HL7 Consumer - Component #2. This channel receives the HL7 messages from
Component #1. It ensures only messages from the Component #1 (HL7 Producer) are processed
via Mirth filter. It then retrieves the Component #1 channel name and patient demographics and
creates a json file - one file per patient.

The result of this project will be found in the OUT folder:
• 5 csv files - original 5 files
• 5 hl7 files - generated by Component #1
• 5 json files - generated by Component #2

