# CBT898
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 898 is a good deal of the life work of Alex Kara.  We     *   FILE 898
//*           are very grateful to him that he wants to share his   *   FILE 898
//*           accumulated knowledge.  Thanks, Alex.                 *   FILE 898
//*                                                                 *   FILE 898
//*     THERE ARE A LOT OF VERY HANDY TOOLS HERE, many of them      *   FILE 898
//*     being quite rare in their functionality.  Alex has spent    *   FILE 898
//*     a lot of time inventing them.  Please look especially at    *   FILE 898
//*     dataset $$ (member list $$MEM) for really good REXX execs   *   FILE 898
//*     and supporting materials.                                   *   FILE 898
//*                                                                 *   FILE 898
//*     Because of the large accumulation of material here, the     *   FILE 898
//*     members of this pds are XMIT-ed PDS'es that are large.      *   FILE 898
//*                                                                 *   FILE 898
//*     Please see members $$README and $$$INDEX to get an idea.    *   FILE 898
//*                                                                 *   FILE 898
//*                email:  alex@karapens.com                        *   FILE 898
//*                                                                 *   FILE 898
//*     - - - - - - - - - - - - - - - - - - - - - - - - - - - - -   *   FILE 898
//*                                                                 *   FILE 898
//*     Background Discussion of Contents  -  from Alex Kara        *   FILE 898
//*     ---------- ---------- -- --------                           *   FILE 898
//*                                                                 *   FILE 898
//*     Just recently I got a tad nostalgic and thought that it     *   FILE 898
//*     would be a shame to let my 35+ years of experience as       *   FILE 898
//*     an appo and sysprog slide into the bit bucket.              *   FILE 898
//*                                                                 *   FILE 898
//*     My experience covered close to 20 years of contracting      *   FILE 898
//*     where I've had contracts for long and short periods at      *   FILE 898
//*     small and large sites (including IBM and CSC).              *   FILE 898
//*     Consequently I have amassed a swag of both handy (and       *   FILE 898
//*     not so handy) routines that I cannot pass on to an          *   FILE 898
//*     understudy/apprentice.  Because of the multiple site        *   FILE 898
//*     support I often had to update my routines as I aimed        *   FILE 898
//*     for generic or easily customisable solutions. As a          *   FILE 898
//*     result I have developed the nasty habit of placing          *   FILE 898
//*     everything into one dataset for the ease of moving that     *   FILE 898
//*     big one around.  I have kept names unique so the            *   FILE 898
//*     dataset contains all my REXX, CLIST, Panels, Skeleton       *   FILE 898
//*     and Message members and a few occasional doco etc..  I      *   FILE 898
//*     do keep a separate dataset for the load library             *   FILE 898
//*     (however, if only 1 or 2 module have changed  I often       *   FILE 898
//*     XMIT that member(s) into an FB=80 dataset and store         *   FILE 898
//*     that as a member in the above catch all and ship).   I      *   FILE 898
//*     hate typing and as it is a catch all I call it              *   FILE 898
//*     'userid.$$' so it is at the top of the DSlist under 3.4     *   FILE 898
//*     and readily accessible).   I identify each member in        *   FILE 898
//*     the $$$INDEX member with a brief 1 line description and     *   FILE 898
//*     with my LINEMAC commands readily edit members from that     *   FILE 898
//*     $$$INDEX member.   This $$ dataset is allocated at the      *   FILE 898
//*     front of all the respective ISPF/SYSEXEC                    *   FILE 898
//*     concatenations.                                             *   FILE 898
//*                                                                 *   FILE 898
//*     I would like to make my knowledge and toils available       *   FILE 898
//*     to all so I am offering the following in the attached       *   FILE 898
//*     ZIP file.  (Already extracted here and put into pds         *   FILE 898
//*     members in XMIT format.  SG)                                *   FILE 898
//*                                                                 *   FILE 898
//*     The individual datasets are XMITted  and called:            *   FILE 898
//*                                                                 *   FILE 898
//*     $$        - non-load module executable  (good               *   FILE 898
//*                 start is the $$README and the $$$INDEX          *   FILE 898
//*                 as further reference).                          *   FILE 898
//*                                                                 *   FILE 898
//*     $LOAD     - load modules                                    *   FILE 898
//*                                                                 *   FILE 898
//*     DSECT     - DSECT maps used for control block               *   FILE 898
//*                 mapping by my memory navigator routine          *   FILE 898
//*                 and on-line disassembler.                       *   FILE 898
//*                                                                 *   FILE 898
//*     ASM       - All the assembler source for load               *   FILE 898
//*                 module used except for those off the            *   FILE 898
//*                 CBT (and PDSEDIT supplied by Fuji back          *   FILE 898
//*                 in 1981   and still working like a              *   FILE 898
//*                 charm for text scans and global                 *   FILE 898
//*                 changes).                                       *   FILE 898
//*                                                                 *   FILE 898
//*     MACLIB    - Contains macros used in assembler               *   FILE 898
//*                 programs                                        *   FILE 898
//*                                                                 *   FILE 898
//*     DB2.UTILS - Examples of REXX commands to execute            *   FILE 898
//*                 functions on DB2 database provided by           *   FILE 898
//*                 some 3PP that may be useful to DBAs.            *   FILE 898
//*                                                                 *   FILE 898
//*     I have extracted  the $README and $$$INDEX and attached     *   FILE 898
//*     them separately for your (or whoever) info.  The $README    *   FILE 898
//*     content is circa Jan 2011 when I was going to make a        *   FILE 898
//*     subset of the better routines (hence the ALLIN1             *   FILE 898
//*     references), however, never eventuated past the doco        *   FILE 898
//*     with my untimely redundancy and the changes made since      *   FILE 898
//*     (today) have been cosmetic blatant spelling/grammar         *   FILE 898
//*     corrections, however, it should give an indication of       *   FILE 898
//*     the highlights and my humble order of preference.  You      *   FILE 898
//*     can see from the list of datasets that the source and       *   FILE 898
//*     loadmods have been XMITted to their own datasets in this    *   FILE 898
//*     packaging.                                                  *   FILE 898
//*                                                                 *   FILE 898
//*     I have no objection in anyone contacting me by phone or     *   FILE 898
//*     email.  I can assist with most queries, however, heavy      *   FILE 898
//*     debugging and customising would be a tad too taxing.        *   FILE 898
//*                                                                 *   FILE 898
//*     Regards,                                                    *   FILE 898
//*     Alex Kara                                                   *   FILE 898
//*     29 McDonald Way                                             *   FILE 898
//*     Churchill                                                   *   FILE 898
//*     VIC  3842                                                   *   FILE 898
//*     Australia                                                   *   FILE 898
//*     alexkara@aussiebb.com.au                                    *   FILE 898
//*     +61 3 5122-3374                                             *   FILE 898
//*                                                                 *   FILE 898
//*     - - - - - - - - - - - - - - - - - - - - - - - - - - - - -   *   FILE 898
//*                                                                 *   FILE 898
//*     Note from Sam Golob:                                        *   FILE 898
//*     ---- ---- --- -----                                         *   FILE 898
//*     I figured out a way to make TAPEMAP show member names for   *   FILE 898
//*     XMIT-format pds'es.  I put the PDS into IEBUPDTE SYSIN      *   FILE 898
//*     (really PDSLOAD) format, delete the data between all the    *   FILE 898
//*     ./ ADD cards, and copy the result into this pds as a        *   FILE 898
//*     member.  TAPEMAP will read this member and display the      *   FILE 898
//*     names from all the ./ ADD NAME=  cards.                     *   FILE 898
//*                                                                 *   FILE 898
//*     These members are marked with a userid of MEMBERS, and are: *   FILE 898
//*                                                                 *   FILE 898
//*     $$MEM    - Member names in $$       XMIT file member        *   FILE 898
//*     ASMMEM   - Member names in ASM      XMIT file member        *   FILE 898
//*     DB2UTMEM - Member names in DB2UTILS XMIT file member        *   FILE 898
//*     MACLIMEM - Member names in MACLIB   XMIT file member        *   FILE 898
//*                                                                 *   FILE 898
```
