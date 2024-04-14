# uefi-raw - [Unreleased]

## Added
- Added `TimestampProtocol`.
- Added `DevicePathToTextProtocol` and `DevicePathFromTextProtocol`.
- Added minor utility methods to `Ipv4Address`: `new(u8, u8, u8, u8) -> Self` and `zero() -> Self`.
- Added `Ip4ModeData`, `Ip4ConfigData`, and `Ip4IcmpType`.

# uefi-raw - 0.5.1 (2024-03-17)

## Added
- Added `IpAddress`, `Ipv4Address`, `Ipv6Address`, and `MacAddress` types.
- Added `ServiceBindingProtocol`, `Dhcp4Protocol`, `HttpProtocol`,
  `Ip4Config2Protocol`, `TlsConfigurationProtocol`, and related types.
- Added `LoadFileProtocol` and `LoadFile2Protocol`.
- Added `firmware_storage` module.

# uefi-raw - 0.5.0 (2023-11-12)

## Added
- Added `AbsolutePointerProtocol`.
- Added `SimpleFileSystemProtocol` and related types.

## Changed
- `{install,reinstall,uninstall}_protocol_interface` now take `const` interface pointers.
- `{un}install_multiple_protocol_interfaces` are now defined as c-variadic
  function pointers. The ABI is `extern "C"` until such time as
  [`extended_varargs_abi_support`](https://github.com/rust-lang/rust/issues/100189)
  is stabilized.
