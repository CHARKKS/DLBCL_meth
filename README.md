## select betameth data for DLBCL
cut -f23,27,166,179,231,346,415,412,737,805,820,854,924,926,1021,1022,49,50,148,150,254,388,401,403,513,725,849,922,923,925,927,983,990,1009 GSE68379_Matrix.processed.txt > DLBCL_meth.txt

## all DLBCL, GCBDLBCL, ABCDLBCL, PMSDLBCL data text file obtained from r (ded.R, charded)

## rename the column head for CGprobeIDs
sed 's/697_AVG.Beta/CGprobeIDs/g' CGprobeIDs.txt > CGprobeIDs_2.txt

## paste the CGprobeID to the meth data files
paste CGprobeIDs_2.txt PMSDLBCL.txt | column -s $'\t' -t > PMSDLBCL_2.txt
paste CGprobeIDs_2.txt GCBDLBCL.txt | column -s $'\t' -t > GCBDLBCL_2.txt
paste CGprobeIDs_2.txt ABCDLBCL.txt | column -s $'\t' -t > ABCDLBCL_2.txt
paste CGprobeIDs_2.txt DLBCL.txt | column -s $'\t' -t > DLBCLmeth_2.txt

## DLBCLpval file obtained from r (ded.R, charded)

## beta0.7_DLBCL
awk '$2 > 0.7 {print $1}' DLBCLmeth_2.txt > A3KAW.txt
awk '$3 > 0.7 {print $1}' DLBCLmeth_2.txt > A4FUK.txt
awk '$4 > 0.7 {print $1}' DLBCLmeth_2.txt > DB.txt
awk '$5 > 0.7 {print $1}' DLBCLmeth_2.txt > DOHH2.txt
awk '$6 > 0.7 {print $1}' DLBCLmeth_2.txt > FARAGE.txt
awk '$7 > 0.7 {print $1}' DLBCLmeth_2.txt > HT.txt
awk '$8 > 0.7 {print $1}' DLBCLmeth_2.txt > KARPAS422.txt
awk '$9 > 0.7 {print $1}' DLBCLmeth_2.txt > KARPAS1106P.txt
awk '$10 > 0.7 {print $1}' DLBCLmeth_2.txt > OCILY19.txt
awk '$11 > 0.7 {print $1}' DLBCLmeth_2.txt > RCK8.txt
awk '$12 > 0.7 {print $1}' DLBCLmeth_2.txt > RL.txt
awk '$13 > 0.7 {print $1}' DLBCLmeth_2.txt > SCI1.txt
awk '$14 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL4.txt
awk '$15 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL6.txt
awk '$16 > 0.7 {print $1}' DLBCLmeth_2.txt > WSUDLCL2.txt
awk '$17 > 0.7 {print $1}' DLBCLmeth_2.txt > WSUNHL.txt
awk '$18 > 0.7 {print $1}' DLBCLmeth_2.txt > BC1.txt
awk '$19 > 0.7 {print $1}' DLBCLmeth_2.txt > BC3.txt
awk '$20 > 0.7 {print $1}' DLBCLmeth_2.txt > CROAP2.txt
awk '$21 > 0.7 {print $1}' DLBCLmeth_2.txt > CTB1.txt
awk '$22 > 0.7 {print $1}' DLBCLmeth_2.txt > GRANTA519.txt
awk '$23 > 0.7 {print $1}' DLBCLmeth_2.txt > JEKO1.txt
awk '$24 > 0.7 {print $1}' DLBCLmeth_2.txt > JM1.txt
awk '$25 > 0.7 {print $1}' DLBCLmeth_2.txt > JSC1.txt
awk '$26 > 0.7 {print $1}' DLBCLmeth_2.txt > MC116.txt
awk '$27 > 0.7 {print $1}' DLBCLmeth_2.txt > NUDUL1.txt
awk '$28 > 0.7 {print $1}' DLBCLmeth_2.txt > SCC3.txt
awk '$29 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL10.txt
awk '$30 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL16.txt
awk '$31 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL5.txt
awk '$32 > 0.7 {print $1}' DLBCLmeth_2.txt > SUDHL8.txt
awk '$33 > 0.7 {print $1}' DLBCLmeth_2.txt > TK.txt
awk '$34 > 0.7 {print $1}' DLBCLmeth_2.txt > TUR.txt
awk '$35 > 0.7 {print $1}' DLBCLmeth_2.txt > VAL.txt

## beta0.3_DLBCL
awk '$2 < 0.3 {print $1}' DLBCLmeth_2.txt > A3KAW.txt
awk '$3 < 0.3 {print $1}' DLBCLmeth_2.txt > A4FUK.txt
awk '$4 < 0.3 {print $1}' DLBCLmeth_2.txt > DB.txt
awk '$5 < 0.3 {print $1}' DLBCLmeth_2.txt > DOHH2.txt
awk '$6 < 0.3 {print $1}' DLBCLmeth_2.txt > FARAGE.txt
awk '$7 < 0.3 {print $1}' DLBCLmeth_2.txt > HT.txt
awk '$8 < 0.3 {print $1}' DLBCLmeth_2.txt > KARPAS422.txt
awk '$9 < 0.3 {print $1}' DLBCLmeth_2.txt > KARPAS1106P.txt
awk '$10 < 0.3 {print $1}' DLBCLmeth_2.txt > OCILY19.txt
awk '$11 < 0.3 {print $1}' DLBCLmeth_2.txt > RCK8.txt
awk '$12 < 0.3 {print $1}' DLBCLmeth_2.txt > RL.txt
awk '$13 < 0.3 {print $1}' DLBCLmeth_2.txt > SCI1.txt
awk '$14 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHL4.txt
awk '$15 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHL6.txt
awk '$16 < 0.3 {print $1}' DLBCLmeth_2.txt > WSUDLCL2.txt
awk '$17 < 0.3 {print $1}' DLBCLmeth_2.txt > WSUNHL.txt
awk '$18 < 0.3 {print $1}' DLBCLmeth_2.txt > BC1.txt
awk '$19 < 0.3 {print $1}' DLBCLmeth_2.txt > BC3.txt
awk '$20 < 0.3 {print $1}' DLBCLmeth_2.txt > CROAP2.txt
awk '$21 < 0.3 {print $1}' DLBCLmeth_2.txt > CTB1.txt
awk '$22 < 0.3 {print $1}' DLBCLmeth_2.txt > GRANTA519.txt
awk '$23 < 0.3 {print $1}' DLBCLmeth_2.txt > JEKO1.txt
awk '$24 < 0.3 {print $1}' DLBCLmeth_2.txt > JM1.txt
awk '$25 < 0.3 {print $1}' DLBCLmeth_2.txt > JSC1.txt
awk '$26 < 0.3 {print $1}' DLBCLmeth_2.txt > MC116.txt
awk '$27 < 0.3 {print $1}' DLBCLmeth_2.txt > NUDUl1.txt
awk '$28 < 0.3 {print $1}' DLBCLmeth_2.txt > SCC3.txt
awk '$29 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHL10.txt
awk '$30 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHL16.txt
awk '$31 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHL5.txt
awk '$32 < 0.3 {print $1}' DLBCLmeth_2.txt > SUDHl8.txt
awk '$33 < 0.3 {print $1}' DLBCLmeth_2.txt > TK.txt
awk '$34 < 0.3 {print $1}' DLBCLmeth_2.txt > TUR.txt
awk '$35 < 0.3 {print $1}' DLBCLmeth_2.txt > VAL.txt
wc -l A3KAW0.3.txt

## beta0.3_DLBCL combine together
awk '$2 < 0.3, $3 <0.3 {print $1,$2,$3}' DLBCLmeth_2.txt > trying.txt (cannot)
paste A3KAW0.3.txt A4FUK0.3.txt DB0.3.txt DOHH20.3.txt FARAGE0.3.txt | column -s $'\t' -t > 1114.txt
awk '{print $1,$3,$5,$7,$9}' 1114.txt | column -s $'\t' -t > 1116.txt
paste 1116.txt HT0.3.txt KARPAS4220.3.txt KARPAS1106P0.3.txt OCILY190.3.txt RCK80.3.txt RL0.3.txt SCI10.3.txt SUDHL40.3.txt SUDHL60.3.txt WSUDLCL20.3.txt WSUNHL0.3.txt BC10.3.txt BC30.3.txt CROAP20.3.txt CTB10.3.txt GRANTA5190.3.txt JEKO10.3.txt JM10.3.txt JSC10.3.txt MC1160.3.txt NUDUL10.3.txt SCC30.3.txt SUDHL100.3.txt SUDHL160.3.txt SUDHL50.3.txt SUDHL80.3.txt TK0.3.txt TUR0.3.txt VAL0.3.txt | column -s $'\t' -t > 1126.txt
awk '{print $1,$2,$3,$4,$5,$6,$8,$10,$12,$14,$16,$18,$20,$22,$24,$26,$28,$30,$32,$34,$36,$38,$40,$42,$44,$46,$48,$50,$52,$54,$56,$58,$60}' 1126.txt | column -s $'\t' -t > 1131.txt

## common lines in the 0.3 files
grep -f VAL0.3.txt TUR0.3.txt > dora.txt (i think it works)
join -j 1 A3KAW0.3.txt A4FUK0.3.txt | awk '{print $1}' > 1154.txt (probably works too??)
comm -1 -2 A3KAW0.3.txt A4FUK0.3.txt > 1216.txt (this is the best)
comm -1 -2 A3KAW.txt A4FUK.txt > 1231.txt (this is the best)
comm -1 -2 A3KAW.txt A4FUK.txt DB.txt DOHH2.txt FARAGE.txt HT.txt KARPAS422.txt KARPAS1106P.txt OCILY19.txt RCK8.txt RL.txt SCI1.txt SUDHL4.txt SUDHL6.txt WSUDLCL2.txt WSUNHL.txt BC1.txt BC3.txt CROAP2.txt CTB1.txt GRANTA519.txt JEKO1.txt JM1.txt JSC1.txt MC116.txt NUDUL1.txt SCC3.txt SUDHL16.txt SUDHL5.txt SUDHL8.txt TK.txt TUR.txt VAL.txt > 1243.txt (doesnt work)
