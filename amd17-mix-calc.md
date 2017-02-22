# AMD17 MIX CALC

Hey guys, I noticed some errors in the mix count.

# INTRO

So according to the current calc, these are all the possible final mixes (96 total)

```
A-1-1-1     B-1-1-1     C-1-1-1     D-1-1-1     E-1-1-1     F-1-1-1
A-1-1-2     B-1-1-2     C-1-1-2     D-1-1-2     E-1-1-2     F-1-1-2
A-1-1-3     B-1-1-3     C-1-1-3     D-1-1-3     E-1-1-3     F-1-1-3
A-1-1-4     B-1-1-4     C-1-1-4     D-1-1-4     E-1-1-4     F-1-1-4
A-1-2-1     B-1-2-1     C-1-2-1     D-1-2-1     E-1-2-1     F-1-2-1
A-1-2-2     B-1-2-2     C-1-2-2     D-1-2-2     E-1-2-2     F-1-2-2
A-1-2-3     B-1-2-3     C-1-2-3     D-1-2-3     E-1-2-3     F-1-2-3
A-1-2-4     B-1-2-4     C-1-2-4     D-1-2-4     E-1-2-4     F-1-2-4
A-2-1-1     B-2-1-1     C-2-1-1     D-2-1-1     E-2-1-1     F-2-1-1
A-2-1-2     B-2-1-2     C-2-1-2     D-2-1-2     E-2-1-2     F-2-1-2
A-2-1-3     B-2-1-3     C-2-1-3     D-2-1-3     E-2-1-3     F-2-1-3
A-2-1-4     B-2-1-4     C-2-1-4     D-2-1-4     E-2-1-4     F-2-1-4
A-2-2-1     B-2-2-1     C-2-2-1     D-2-2-1     E-2-2-1     F-2-2-1
A-2-2-2     B-2-2-2     C-2-2-2     D-2-2-2     E-2-2-2     F-2-2-2
A-2-2-3     B-2-2-3     C-2-2-3     D-2-2-3     E-2-2-3     F-2-2-3
A-2-2-4     B-2-2-4     C-2-2-4     D-2-2-4     E-2-2-4     F-2-2-4
```


# ISSUE 1 - BEFORE COMPLETING THE FULL SELECTION

## EXAMPLE - STAGE 1
When the user is selecting the genre in Stage 1, they should not hear 'A-1-1-1', they should hear simply 'A'.


## EXAMPLE - STAGE 2
And for example, if a user selected Genre A, and they are now in Stage 2 selecting between night or day, they should not hear A-1-1-1 or A-2-1-1, they should hear simply A-1 or A-2.


In this way, we actually need the following mixes for stages 1 to 3:

```
A           B           C           D           E           F

A-1         B-1         C-1         D-1         E-1         F-1
A-2         B-2         C-2         D-2         E-2         F-2

A-1-1       B-1-1       C-1-1       D-1-1       E-1-1       F-1-1
A-1-2       B-1-2       C-1-2       D-1-2       E-1-2       F-1-2
A-2-1       B-2-1       C-2-1       D-2-1       E-2-1       F-2-1
A-2-2       B-2-2       C-2-2       D-2-2       E-2-2       F-2-2
```

## INTERMEDIARY COUNT

That means for each stage, we need these:

```
Stage 1 - 6 10s loops
Stage 2 - 12 10s loops
Stage 3 - 24 10s loops
```

That is an additional 42 10s loop intermediary mixes that must be prepared.


# ISSUE 2 - STAGE 4 ALLOWS MULTI-SELECT, UP TO 2 OPTIONS

This was news to me, I heard you guys actually wanted to let users choose **UP TO 2** options out of the 4 options in Stage 4.

This means in stage 4, instead of simply 4 options

```
1
2
3
4
```

there are actually 10 options

```
1
2
3
4
12
13
14
23
24
34
```

that means the final mixes are actually

```
A-1-1-1     B-1-1-1     C-1-1-1     D-1-1-1     E-1-1-1     F-1-1-1
A-1-1-2     B-1-1-2     C-1-1-2     D-1-1-2     E-1-1-2     F-1-1-2
A-1-1-3     B-1-1-3     C-1-1-3     D-1-1-3     E-1-1-3     F-1-1-3
A-1-1-4     B-1-1-4     C-1-1-4     D-1-1-4     E-1-1-4     F-1-1-4
A-1-1-12    B-1-1-12    C-1-1-12    D-1-1-12    E-1-1-12    F-1-1-12
A-1-1-13    B-1-1-13    C-1-1-13    D-1-1-13    E-1-1-13    F-1-1-13
A-1-1-14    B-1-1-14    C-1-1-14    D-1-1-14    E-1-1-14    F-1-1-14
A-1-1-23    B-1-1-23    C-1-1-23    D-1-1-23    E-1-1-23    F-1-1-23
A-1-1-24    B-1-1-24    C-1-1-24    D-1-1-24    E-1-1-24    F-1-1-24
A-1-1-34    B-1-1-34    C-1-1-34    D-1-1-34    E-1-1-34    F-1-1-34

A-1-2-1     B-1-2-1     C-1-2-1     D-1-2-1     E-1-2-1     F-1-2-1
A-1-2-2     B-1-2-2     C-1-2-2     D-1-2-2     E-1-2-2     F-1-2-2
A-1-2-3     B-1-2-3     C-1-2-3     D-1-2-3     E-1-2-3     F-1-2-3
A-1-2-4     B-1-2-4     C-1-2-4     D-1-2-4     E-1-2-4     F-1-2-4
A-1-2-12    B-1-2-12    C-1-2-12    D-1-2-12    E-1-2-12    F-1-2-12
A-1-2-13    B-1-2-13    C-1-2-13    D-1-2-13    E-1-2-13    F-1-2-13
A-1-2-14    B-1-2-14    C-1-2-14    D-1-2-14    E-1-2-14    F-1-2-14
A-1-2-23    B-1-2-23    C-1-2-23    D-1-2-23    E-1-2-23    F-1-2-23
A-1-2-24    B-1-2-24    C-1-2-24    D-1-2-24    E-1-2-24    F-1-2-24
A-1-2-34    B-1-2-34    C-1-2-34    D-1-2-34    E-1-2-34    F-1-2-34

A-2-1-1     B-2-1-1     C-2-1-1     D-2-1-1     E-2-1-1     F-2-1-1
A-2-1-2     B-2-1-2     C-2-1-2     D-2-1-2     E-2-1-2     F-2-1-2
A-2-1-3     B-2-1-3     C-2-1-3     D-2-1-3     E-2-1-3     F-2-1-3
A-2-1-4     B-2-1-4     C-2-1-4     D-2-1-4     E-2-1-4     F-2-1-4
A-2-1-12    B-2-1-12    C-2-1-12    D-2-1-12    E-2-1-12    F-2-1-12
A-2-1-13    B-2-1-13    C-2-1-13    D-2-1-13    E-2-1-13    F-2-1-13
A-2-1-14    B-2-1-14    C-2-1-14    D-2-1-14    E-2-1-14    F-2-1-14
A-2-1-23    B-2-1-23    C-2-1-23    D-2-1-23    E-2-1-23    F-2-1-23
A-2-1-24    B-2-1-24    C-2-1-24    D-2-1-24    E-2-1-24    F-2-1-24
A-2-1-34    B-2-1-34    C-2-1-34    D-2-1-34    E-2-1-34    F-2-1-34

A-2-2-1     B-2-2-1     C-2-2-1     D-2-2-1     E-2-2-1     F-2-2-1
A-2-2-2     B-2-2-2     C-2-2-2     D-2-2-2     E-2-2-2     F-2-2-2
A-2-2-3     B-2-2-3     C-2-2-3     D-2-2-3     E-2-2-3     F-2-2-3
A-2-2-4     B-2-2-4     C-2-2-4     D-2-2-4     E-2-2-4     F-2-2-4
A-2-2-12    B-2-2-12    C-2-2-12    D-2-2-12    E-2-2-12    F-2-2-12
A-2-2-13    B-2-2-13    C-2-2-13    D-2-2-13    E-2-2-13    F-2-2-13
A-2-2-14    B-2-2-14    C-2-2-14    D-2-2-14    E-2-2-14    F-2-2-14
A-2-2-23    B-2-2-23    C-2-2-23    D-2-2-23    E-2-2-23    F-2-2-23
A-2-2-24    B-2-2-24    C-2-2-24    D-2-2-24    E-2-2-24    F-2-2-24
A-2-2-34    B-2-2-34    C-2-2-34    D-2-2-34    E-2-2-34    F-2-2-34
```

For a total of 240 final mixes.

# FINAL COUNT

So the files that will need to be created are:

```
Stage 1 - 6 10s loops
Stage 2 - 12 10s loops
Stage 3 - 24 10s loops
Stage 4 - 240 10s loops
Complete - 240 full tracks
```

