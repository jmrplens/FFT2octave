# FFT2octave
Matlab. Filter FFT data to octave-band and fractional octave-band.


## Use

```matlab
[Oct,fc,fl,fu] = FFT2octave(f,fftdata,b,varargin)
```

The first two inputs are the FFT, `f` is the frequency array and `fftdata` is the fft values.

The third input is the bandwidth:

- `b=1` One-octave band.
- `b=3` Third-octave band.
- `b=2` Half-octave band.
- `b=3/2` 2/3-octave band.
- `b=24` 1/24-octave band.

**Optional inputs**

The fourth input indicates whether the FFT data is linear `''` or logarithmic `'dB'`.

The fifth input only affects when the value of `b` is 1 or 3. It indicates whether you want the normalized or calculated frequencies. By default they are calculated (`false`).

## Examples of use

```matlab
% To get in one-octave frequencies
[Oct,fc,fl,fu] = FFT2octave(f,fftdata,1)
```

```matlab
% To get in one-octave frequencies if the data is in dB
[Oct,fc,fl,fu] = FFT2octave(f,fftdata,1,'dB')
```

```matlab
% To get in one-octave frequencies normalized if the data is in dB
[Oct,fc,fl,fu] = FFT2octave(f,fftdata,1,'dB',true)
```

```matlab
% To get in third-octave frequencies
[Oct,fc,fl,fu] = FFT2octave(f,fftdata,3)
```
