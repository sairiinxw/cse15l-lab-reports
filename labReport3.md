# Lab Report 3: Bugs and Commands

## Part 1: Bugs

## Part 2: Researching Commands

### `find`: 4 command-line options used on files and directories from `./technical`
**Using `find -regex`**
*Example 1 command and output on `./technical/911report` directory
```
Cyrene@charless-MacBook-Pro technical % find 911report -regex ".*chapter.*"
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
*What it's doing and why it's useful: It finds all path names in this `./technical/911report` directory containing the pattern chapter in the path name. It's useful for finding a path that you need for a file or directory.
\
\
*Example 2 command and output on `./technical/911report/chapter-1.txt` file.
```
Cyrene@charless-MacBook-Pro technical % find 911report/chapter-1.txt -regex ".*chapter.*"
911report/chapter-1.txt
```
*What it's doing and why it's useful: It just prints out the path to the file you use find -regex on. This could be useful for finding a specific file path from the working directory, but it's hard to see how it can be helpful when you already need the path for the command line.
\
\
**Using `find -mmin`**
*Example 1 command and output on `./technical/911report` directory
```
Cyrene@charless-MacBook-Pro technical % find 911report -mmin -60
911report
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
*What it's doing and why it's useful: It finds and prints out a path name list of all files and directories last modified in the last 60 minutes in the working directory. Since I just cloned the directory, all of these were modified within 60 minutes. This is useful for finding out what files were recently modified and could be used to double-check a deadline.
\
\
*Example 2 command and output on `./technical/911report/chapter-2.txt` file
```
Cyrene@charless-MacBook-Pro technical % find 911report/chapter-2.txt -mmin -60
911report/chapter-2.txt
```
*What it's doing and why it's useful: It just prints out the path name of the file you use find -mmin -60 on because `chapter-2.txt` was modified within the last 60 minutes when I created the directory. However, if I didn't modify it recently, it would probably not show anything. This could be useful for checking if that specific file was modified recently.
\
\
**Using `find -exec {} \;`**
*Example 1 command and output on `./technical/911report` directory
```
find 911report -name "chapter-13*" -exec grep terrorist {} \;
                to his abiding interest in carrying out terrorist operations. Although KSM claims
                providing funds to JI for terrorist operations as early as 1999. Intelligence
                involving himself in al Qaeda's broader terrorist program. Indeed, KSM describes
                security practice dictated that no senior member could manage terrorist activities
                On Nashiri's idea for his first terrorist operation and his travels, see
                be one of al Qaeda's most committed terrorists and, according to one of his
                commit a terrorist act 'in Mecca inside the Ka'aba itself ' [the holiest site in
                Arabia in 1999 and 2000 to meet with Saudi officials on terrorist financing. These
                from biological and chemical weapons. President Clinton repeatedly linked terrorist
                (I. B. Tauris, 2003), p. 188. Khaldan and Derunta were terrorist training camps in
                it essential for waging terrorist operations and guerrilla warfare in the jihad
                member, instructor, and technical guru for the Khaldan and Derunta terrorist
                register with the Taliban. See NSC memo, Berger to President Clinton, terrorist
                years in prison in France for activities related to association with terrorist
            32. NSC memo, Berger to President Clinton, terrorist threat at the millennium, Dec.
                foreign leaders to maintain pressure on terrorists. See CIA briefing
                relate specifically to terrorist financing. Another witness recalled that the UBL
                the problem to the CIA's separation of terrorist-financing analysis from other
                devoted to the analysis of all financial issues, including terrorist financing.
                it dealt with an array of issues besides terrorist financing, including drug
                analysts were separated from the operational side of terrorist financing at CTC,
                terrorist financing proposals were a good option, so Treasury continued to plan to
                names (and aliases) of terrorists were collected and disseminated to State, INS, and
                bombing the destroyer, saying:"Any would-be terrorist out there needs to know that
                this phrase in May 2001, when warnings of terrorist threats began to multiply.
                confusion about where Bin Ladin fit into U.S.-Taliban relations-the Saudi terrorist
                manipulation that would conclusively link the document with a terrorist
                money for the Palestinian terrorist group Hamas. Sources alleged that Aulaqi had
            128. Intelligence report, Hezbollah and Sunni terrorist activities, Sept. 21, 2001;
                and Prospects,"Dec. 2000). Clarke had also mentioned domestic terrorist cells in
                explosion, the terrorist would be likely to prefer a domestic hijacking. Between
                available was one not often used pre-9/11 for suspected terrorists: an FBI BOLO (be
                Medical Examiner's Office, the WTC attacks killed 2,749 nonterrorists, including
                nonterrorist occupants of the hijacked aircraft. New York City Office of the Chief
                Pentagon attack killed 184 nonterrorists, including the occupants of the hijacked
                nonterrorists died in the crash of United Airlines Flight 93 in Pennsylvania. FBI
                assumption that everybody kind of shared was that it was global terrorists. . . . I
                they had any recent contact with Usama Bin Ladin or knew anything about terrorist
                derogatory information on either person linking them to terrorist activity. Their
                TIPOFF terrorist watchlist was checked by the FBI, the Terrorist Screening Center
                preventing terrorists from acquiring weapons of mass destruction, see White House
                The author suggested instead hitting terrorists outside the Middle East in the
                or Southeast Asia might be a surprise to the terrorists. The memo may have been a
            7. For Pakistan playing a key role in apprehending 500 terrorists, see Richard
            30. For terrorists being self-funding, see United Nations report, "Second Report of
                been watchlisted, their terrorist affiliations could have been exposed either at the
                standards are among the vulnerabilities exploited by terrorists, possibly including
                and the DCI's Counterterrorist Center (CTC) should be concentrated more effectively
             The DCI's Counterterrorist Center would become a CIA unit, to handle the direction
                foreign intelligence about the terrorist enemy.
                transnational terrorist organizations: their people, goals, strategies,
            In our proposal, that reservoir of institutional memory about terrorist organizations
                    terrorists across the foreign-domestic divide with a National Counterterrorism
                Counterterrorist Center that played such a key role before 9/11. A third major
                    Counterterrorist Center at CIA, for example, recruits liaison officers from
                    transnational terrorist organizations with global reach. It should develop net
                    Counterterrorist Center and the DIA's Joint Intelligence Task Force-Combatting
                Consider this hypothetical case. The NSA discovers that a suspected terrorist is
                    terrorist personalities, organizations, and possible means of attack.
                    on counterterrorism, specifically including the head of the Counterterrorist
                provide reasonable security against major terrorist acts within the United States
                agency for the investigation of foreign terrorist groups operating inside the United
                    target, the full range of investigative tools against a suspected terrorist can
                has the job to map "terrorist threats to the homeland against our assessed
                vulnerabilities in order to drive our efforts to protect against terrorist
                community had gathered intelligence on the possibility that terrorists might turn to
                Airlines), we found no evidence that the terrorists targeted particular airports or
                terrorists' targeting: they simply booked heavily fueled east-to-west
                interview (Nov. 21, 2003); UAL report, "United dispatch SMFDO activities-terrorist
                which a terrorist group loaded a Learjet with explosives and took off for a suicide
                military's response to the real-world terrorist attack on 9/11. According to General
                teleconference for a domestic terrorist attack. NMCC and National Military Joint
            61. Because the U.S. embassy in Khartoum had been closed in response to terrorist
                Efforts Along the Northern Border," Apr. 2000 (inspection plan). On terrorists
                concerns about discrimination and to deter terrorists from figuring out the
                terrorists), see DOS cable, State 182167, "Fighting Terrorism: Visas Viper
                the terrorist from others around the world who had his or her name. In addition, the
                preparedness and response to terrorist attack. Though the intelligence oversight
                domestic terrorist attacks and recommended a new institution devoted to identifying
                Intelligence Advisory Board, focused specifically on terrorist threats and what
            1. On financing of Egyptian terrorists, see Intelligence report, Sudanese links to
                its Sudanese wing, July 22, 1993. On aid to Yemeni terrorists, see DOS memo,
                (Dec. 30, 1996; Jan. 3, 1997); on connections and collaboration with other terrorist
                terrorist groups, in 1993 the U.S. government designated the country a state sponsor
                that the embassy was an excellent vehicle for gathering information on terrorists.
                designated a "foreign terrorist organization" also brings sanctions and stigmatizes
                32 terrorists to justice since July 1998, more than half of whom were al Qaeda. CIA
```
*What it's doing and why it's useful: It's printing all lines with the word "terrorist" in each file with path name "chapter-13" in the `./technical/911report` directory. This is useful for narrowing down searching code in a directory.
\
\
*Example 2 command and output on `./technical/911report/chapter-3.txt` file
```
Cyrene@charless-MacBook-Pro technical % find 911report/chapter-3.txt -exec grep Hoover {} \;    
                looming, President Franklin D. Roosevelt ordered FBI Director J. Edgar Hoover to
                Hoover added investigation of possible espionage, sabotage, or subversion to the
                the newly established Central Intelligence Agency. Hoover jealously guarded the
                FBI's domestic portfolio against all rivals. Hoover felt he was accountable only to
                in the 1970s. Two years after Hoover's death in 1972, congresCOUNTERTERRORISM
                especially individuals whom Hoover wanted to discredit (notably the Reverend Martin
```
*What it's doing and why it's useful: It's searching for all lines with "Hoover" on each file. Since the command was used on a file, `-exec grep {} \;` only accesses `chapter-3.txt`. This is useful for finding specific lines in a file, but it's not very necessary when we can use grep.
\
\
**Using `find -maxdepth`**
*Example 1 command and output on `./technical` directory
```
Cyrene@charless-MacBook-Pro technical % find . -maxdepth 2 -type d
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
*What it's doing and why it's useful: It finds all directories, but limits the depth of searches to 2 directories descended. This is useful for limiting your search of all directories if there are too many directories within the one you're looking at.
\
\
*Example 2 command and output
```
Cyrene@charless-MacBook-Pro technical % find 911report/preface.txt -maxdepth 2        
911report/preface.txt
```
*What it's doing and why it's useful: It's just printing out the file I'm using find on. Since I'm not using the command on a directory, it doesn't realy matter what the maxdepth is because there are no directories within a file. This is not really useful I think.
\
\
**Sources**
[Red Hat] (https://www.redhat.com/sysadmin/linux-find-command)
[IBM] (https://www.ibm.com/docs/pl/aix/7.1?topic=f-find-command)
