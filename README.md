# GA-G41MT-S2PT-Rev-1.1-DSDT-Patch
GA-G41MT-S2PT Rev 1.1 DSDT Patches

So I’ve been working on a DSDT for the GA-G41MT-S2PT Revision 1.1 which
can be added to MaciASL under Repo section.

Note that ALC889 patch will not work on Revision 2.0 which uses VIA
Audio Chip.  Revision 1.1 Uses ALC889. Revision 1.0 & 2.1 has ALC887.

MaciASL needs to be on ACPI 6.1 under iASL which is set to default when
downloading MaciASL from RehabMans fork.

Ive done the following patches for HPET, LPC ICH7, SMBUS, Shutdown and
WAK fixes.

The patches which are important for this board is HPET and LPC ICH7
without those too patches you will see Kernel Panics relating to
AppleIntelCPUPowermanagement.

Patches for ALC889 uses Audio ID 1 which is the most easiest for Clover
Hotpatch.

Shutdown Fix is to fix shutdown issues which this board does not
shutdown without this patch.

You will need to Drop OEM_DSM in Config.plist for Clover.

For PowerManagement.

Core 2 CPUs only requires Generate C and P States which can be added in
Config.plist.
