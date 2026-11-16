# Vendored eufy-mega-client (C220 fork)

`keesmod-eufy-mega-client-0.30.3-c220.1.tgz` is upstream
[eufy-mega-client](https://github.com/keesmod/eufy-mega-client) 0.30.3 with one
change: the Indoor Cam C220 (`T8W11C`, device type `10010`) under a HomeBase 3
(`T8030`) is admitted with the same HomeBase 3 media policy as the other indoor
cameras. See `eufy-mega-client-c220.patch` for the exact diff.

The vendor layer already routes type 10010 (`INDOOR_PT_CAMERA_C220_V2`) through
the HomeBase livestream path; only the exact admission entry was missing.

Rebuild: apply the patch to eufy-mega-client 0.30.3, set the version to
`0.30.3-c220.1`, run `npm pack`, and copy the tarball here.
