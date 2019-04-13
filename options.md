# Options / Additional Info
This represents some effort made to reverse enginner configuration options, and
to document key mappings, both by brute force and by using information
resulting from sniffing raw bluetooth commands by lentinj

See: https://github.com/lentinj/tp-compact-keyboard/

## Fn Keys
- `Fn + P` - Pause
- `Fn + B` - Break
- `Fn + S` - SysRq
- `Fn + K` - Scroll Lock
- `Fn + Del` - Enter pairing mode
- `Fn + Esc` - FnLk (requires userspace utility)

## 0x00: ???

## 0x01: Media Keys
```
0 - f5 f6 f7 f8 f9 f10 f11 f12
1 - f5 f6 f7 f8 f9 f10 f11 f12
2 - f5 f6 f7 f8 f9 f10 f11 f12
3 - f5 f6 f7 f8 f9 f10 f11
4 - f5 f6 f7 f8 f9 f10 f11 f12
5 - f5 f6 f7 f8 f9 f10
6 - f5 f6 f7 f8 f9 f10 f11 f12
7 - f5 f6       f9 f10
8 -                f10
9 - f5 f6 f7 f8 f9 f10 f11 f12
a - f5 f6 f7 f8 f9 f10 f11 f12
b - f5 f6 f7 f8 f9 f10 f11 f12
c - f5 f6 f7 f8 f9 f10 f11 f12
d - f5 f6 f7 f8 f9 f10 f11 f12
e - f5 f6 f7 f8 f9 f10 f11 f12
f - f5 f6 f7 f8 f9 f10 f11 f12
```

## 0x02: TrackPoint Sensitivity
```
N. - Base Speed
.N - Sensitivity

0 - Min
...
f - Max
```

## 0x03: ???

## 0x04: ???
```
0 - Returns: 17 12 03 00 ...
```

## 0x05: Fn-Lock
```
0 - Off - Media keys default;   F-keys behind Fn
1 - On  - Media keys behind Fn; F-keys default
```

## 0x06: ???

## 0x07: ??? - Only seems to function if `0x01` is set to `0x08`
```
0 - ???
1 - Returns: (toggle)
    - 17 00 ...
      11 00

    - 17 00 ...
      11 c6
```

## 0x08: ???
```
0 - ???
1 - Returns:
    - 17 00 ...
      10 f3 03
```

## 0x09: TrackPoint Middle-Button
```
0 - Middle-Click and Scroll Enabled  + Custom Response Enabled
1 - Middle-Click and Scroll Disabled + Custom Response Enabled
```
