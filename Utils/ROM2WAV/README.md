# BIN2WAV Conversion
## Note
Remove "macos155" file extension when running on MacOS terminal

## Example Output 1
```
% ./bin2wav -h            

BIN to WAV (Jun 17 2025) win32-version by CoolHacker, algo by svofski.
Compiled for MacOS 15.5 with minor fix by the Clueless Engineer.

Usage: bin2wav program.rom program.wav [options]
   -s load_addr in C-like notation e.g. 256, 0x100. Default 0x100.
   -n tape_name for Vector-06C name to put in tape headers. Default: rom file name
   -m machine-format (default v06c-rom)
Available formats:
   rk-bin          Радио 86РК
   mikrosha-bin    Микроша
   partner-bin     Партнер
   v06c-rom        Вектор-06ц
   krista-rom      Криста-2
   specialist-rks  Специалист .RKS
   specialist-mon  Специалист .MON
```
## Example Output 2
```
% ./bin2wav rockford.rom rockford.wav
Input file:    rockford.rom
Output file:   rockford.wav
Load address:  0x0100
Tape name:     rockford.rom
Tape format:   v06c-rom
WAV file written to rockford.wav
```
