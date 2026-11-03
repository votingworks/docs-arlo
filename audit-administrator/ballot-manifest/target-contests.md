# Target Contests

The target contests are the required contests to be audited.  Target contests will drive the ballot retrieval sample size and require the risk limit to be met.

{% tabs %}
{% tab title="Ballot Polling/Batch Comparison/Hybrid" icon="bullseye-arrow" %}
For each targeted contest, you’ll enter the contest name, number of winners, number of votes allowed, the name and votes for each candidate, and total number of ballots cast (not required for batch comparison). \
\
Write-in candidates should also be included if any were awarded votes. Generally only a single "Write-In Candidate" category is needed.\
\
The total ballot cards cast _**should be the total number of ballots in your ballot manifest**_, even ballots that do not contain the contest.

{% hint style="warning" %}
**Note:** for **hybrid** audits, the Contest Name field will be a drop down menu populated from the standardized contest file. &#x20;

For **batch comparison** audits, the Names of Candidates/Choices will drive the required candidate headers in the contest totals by batch file. The [candidate totals by batch file'](../../jurisdiction-manager/pre-audit-file-uploads/candidate-totals-by-batch.md)s headers must match the candidate names entered at this step.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

If a contest has more than two choices, select Add a new candidate/choice to add more lines.

{% hint style="warning" %}
**Note:** Batch comparison audit setup also includes a box for "pending ballots." Include the number of pending ballots in rare circumstances where not all ballots can be included prior to the audit start (i.e. a court order, problems in processing, etc.). Consult with a VotingWorks support person before using this feature.

![](<../../.gitbook/assets/image (1).png>)
{% endhint %}

{% hint style="warning" %}
**Contests Subject to Runoff Laws:** For these contests, check the Runoff Law box when entering the contest. Only check this box when auditing a contest that has advanced to a runoff.

<img src="../../.gitbook/assets/Screenshot 2026-10-30 at 2.56.30 PM.png" alt="" data-size="original">
{% endhint %}

The last step in setting up a target contest is choosing which jurisdictions have that contest on the ballot.

1. **Select the Select Jurisdictions button.**
2. **Choose the jurisdictions.** If the contest is in every jurisdiction, check the Select all box. Otherwise, check each jurisdiction that has the contest.
3. **Select Save & Next.**

{% hint style="warning" %}
If you’re auditing more than one contest, **select Add Contest** for additional targeted contest before you **select Save & Next.**<br>
{% endhint %}

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Ballot Comparison" icon="bullseye-arrow" %}
Arlo populates the contests based on the standardized contest file. Simply select the contest(s) being targeted from the list.

![](<../../.gitbook/assets/image (40).png>)

Click Save & Next when finished.
{% endtab %}
{% endtabs %}
