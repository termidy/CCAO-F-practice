# The checked complaint summary

From the practice "Three Steps and a Check Between Them" (Section 2): Claude's step-1 summary of `files/complaint-log.csv`,
as it came in the recorded run, then checked against the CSV. Use it if you join after Section 2 or did not keep your
own chat.

Check result: the counts are right. The five late complaints (43 to 56 days after delivery), the six damaged records
with no delivery date and the duplicate (CL-0024 and CL-0025) match the file. Keep the six undated records as a stated
limit in anything you build on this summary.

## The summary


- [count] The file has 85 records, but CL-0024 and CL-0025 are the same order (DH-301558) logged twice, so there are 84 distinct complaints. Counts below use all 85 rows unless stated.
- [count] Reasons: damaged 37 (43.5%), changed_mind 34 (40.0%), wrong_item 14 (16.5%). CL-0069 is coded “Damaged” with a capital D, and I counted it as damaged. Without the duplicate, damaged is 36.
- [count] Of the 37 damaged records, 31 have a delivery date. One of those is the duplicate, so the timing figures below use 30 distinct complaints.
- [count] Damaged complaints came a median of 5 days after delivery (mean 12.8, range 0 to 56). Four came on the delivery day or the next day (CL-0002, CL-0044, CL-0014, CL-0055).
- [count] 22 of the 30 came within 8 days of delivery, and 25 within 19 days. The other 5 came after 43, 44, 49, 54 and 56 days (CL-0043, CL-0080, CL-0028, CL-0011, CL-0018).
- [inference] The delays split into two groups: most customers report damage within about a week, and a small group reports it 6 to 8 weeks later. Nothing in the file shows nothing in the data explains the late group, so the reason for the gap is a guess.
- [count] 6 damaged records have no delivery date (CL-0038, 0040, 0049, 0050, 0051, 0052) and are left out of the timing figures.
- [inference] The summary text sometimes doesn’t fit the product. CL-0065 (oak side table) mentions a bent hinge, CL-0049 (glass pendant shade) a broken switch housing, and CL-0020 (cast iron skillet) thin fabric. I used reason_code as recorded, but the free-text field may be unreliable. I did not calculate delivery-to-complaint timing for changed_mind or wrong_item.



