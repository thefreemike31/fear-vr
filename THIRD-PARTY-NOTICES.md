# Third-party notices

This F.E.A.R. VR package contains or incorporates:

- DxWrapper, pinned at commit
  `9ef1464462490c2469a15aff27528a8eed801cd5`, with the F.E.A.R. VR ResetEx and
  DirectSound/EAX integration patches. Its complete multi-license notice is
  included as `licenses\dxwrapper.txt`.
- DxWrapper's graphics bootstrap stub, installed on Steam, with its separate
  notice included as `licenses\DxWrapper-Stub.txt`.
- DSOAL r444, used as the DirectSound3D and EAX compatibility runtime. Its
  license is included as `licenses\DSOAL.txt`.
- OpenAL Soft 1.23.1, used as DSOAL's Win32 software audio backend. Its license
  is included as `licenses\OpenAL-Soft.txt`.
- Khronos OpenXR Loader 1.1.54, statically linked into `fearvr_bridge.dll`,
  under Apache-2.0. Its notice is included as
  `licenses\OpenXR-Loader.txt`.
- MinHook 1.3.4, statically linked into `fearvr_bridge.dll`, under BSD-2-Clause
  and its included HDE notices. Its notice is included as
  `licenses\MinHook.txt`.
- JsonCpp 1.9.6, statically linked through the OpenXR loader, under its
  public-domain/MIT terms. Its notice is included as
  `licenses\JsonCpp.txt`.
- WebXR Input Profiles controller meshes, pinned at commit
  `f4992299601614adbfefd398dc8e281556bb7444`, used to generate calibration
  outlines under MIT. Their notice is included as
  `licenses\WebXR-Input-Profiles.txt`. Controller names identify the hardware;
  they do not imply manufacturer endorsement.

The reconstructed F.E.A.R. Public Tools runtime modules remain subject to the
terms supplied with those tools. F.E.A.R. and related assets remain the property
of their respective owners. The mod is distributed free of charge under the
permission reported by the project maintainer; this package grants no right to
redistribute the original game or use its assets outside that permission.

## zlib

The launcher language importer statically links zlib for bounded archive decompression.
Copyright and license: `licenses/zlib.txt`. No game-language data is redistributed.
