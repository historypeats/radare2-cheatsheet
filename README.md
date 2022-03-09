## Run binary with radare2 and attach debugger
r2 -AA -d binary

## Restart binary
oo

## Restart binary and attach debugger
ood

## List functions
afl

## Disassemble function
pdf @ <func>
example: ```pdf @ sym.main```

## Print call graph
agc > /tmp/foo.dot xdot /tmp/foo.dot

## Print a detailed graph
ag $$ > /tmp/c2.dot

## Disassemble instruction
pD 2

## Show call graph of function
VV @ sym.main

## Expressions let us do math and stuff via cmdline
? 0x8 + 4

## Seek to a specific memory location
s 0x08048470

## write hex value
wx eb

## Debugging/Visual Mode
https://book.rada.re/first_steps/basic_debugger_session.html


## Set breakpoint
db 0x00401383

## Remove breakpoint
db -0x00401383

## List breakpoints
db 

## Continue execution
dc

## Switch to Visual Mode
V

## Cycle through Visual modes
p

## Step through code
s

## Switch to graph view (in Visual Mode)
V

## Get strings
rabin2 -z file

## Pattern generation
ragg2 -p 300 -r

## Get assembly instruction
rasm2 -a x86 -b 32 'jmp 16'
