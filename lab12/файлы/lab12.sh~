#!/bin/bash
while getopts i:o:pCn optletter
do case $optletter in
       i) iflag=1; ival=$OPTARG;;
       o) oflag=1; oval=$OPTARG;;
       p) pflag=1; pval=$OPTARG;;
       C) Cflag=1;;
       n) nflag=1;;
       *) echo Illegalopttion $optletter
   esac
done
if (((cflag==1)&&(nflag==1)))
then  grep -e${pval} -i -n ${ival}
      if ((oflag==1))
      then grep -e${pval} -i -n ${ival} > ${oval}
      fi
fi
if (((cflag==1)&&(nflag==0)))
then grep -e${pval} -i ${ival}
     if (oflag==1)
     then grep -e${pval} -i ${ival} > ${oval}
     fi
fi
if (((cflag==0)&&(nflag==1)))
then grep -e${pval} -i ${ival}
     if (oflag==1)
     then grep -e${pval} -n ${ival} > ${oval}
     fi
fi
if (((cflag==0)&&(nflag==0)))
then grep -e${pval} -i ${ival}
     if (oflag==1)
     then grep -e${pval} ${ival} > ${oval}
     fi
fi
