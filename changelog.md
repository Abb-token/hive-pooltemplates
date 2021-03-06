##### 0.6-161@200924-2 2020-09-24
*   Fixed `nvidia-driver-update` tool (changed search order for download links, fixed installation for release version numbering)

##### 0.6-160@200924 2020-09-24
*   Improved `nvidia-driver-update` tool (added support for new version numbering e.g. 455.23.04)
*   Improved hashrate WD (added condition for check hashrate only if connection is available)
*   Some workaround for AMD iGPUs "Picasso" (exclusion from GPU stats and OC)
*   Gminer v2.23 (improved performance for KawPoW algorithm, improved performance of DAG file generation, fixed "no shares" bug for Cuckoo Cycle algorithms when intensity less than 100%)
*   miniZ v1.6w (major improvements on 150/5  2-20%, depending on GPU, higher on Turing cards, added ocX table to telemetry)
*   XMRig v6.3.4 (misc improvements for RandomX)
*   CPUminer-Opt-X11K v3.14.3 (fork with x11k implementation)
*   CPUminer-Opt-rplant v4.5.16 (added x33 algo)
*   WildRig-Multi v0.27.3 (implemented x11k (Kyancoin), x33 (Qureno), vprogpow (new algo of VeriBlock), added parameter '--protocol' (ethproxy, ethstratum, stratum, stratum1, stratum2, ufo, ufo2), added parameter '--no-dag-split', fixed '--ptx-version parameter', fixed RTX 3080/3090 support, fixed incorrect shares on progpow variants after devfee)

##### 0.6-159@200918 2020-09-18
*   Added 'agent' configuration sync after loosing connection to Hive API servers
*   Improved DoH [DNS-over-HTTPS] implementation (added service control from web interface, added AliDNS servers)
*   Minor fixes for VBIOS flashing procedure (fixed mem size reporting for GPU with 10Gb+, fixed empty Nvidia flashing log, fixed issue of no reboot after successful flashing)
*   T-Rex v0.17.2 (added ethash and progpowz algos; add 'gpu-init-mode' parameter: enables sequential DAG generation to reduce load on power supplies, print hash rate if no shares have been found for more than 1 minute to indicate miner's activity; bugs fixes: CUDA 11 build not working on some algorithms and RTX cards, GPU is idle error when generating DAG on low-end cards)
*   WildRig-Multi v0.26.0 (implemented megabtx, megamec and minotaur algos; added default --opencl-launch for p102, p104 and p106 gpu's)
*   Bminer v16.3.1 (enable tuning memory timings for Ethash on NVIDIA GPUs via the '-fast' option)
*   SRBMiner-Multi v0.5.2 (added 'verushash' for GPU mining, 'verushash' on CPU optimised a little bit, 'ethash' on GPU optimised a little bit, removed 'MTP' algo)

##### 0.6-158@200913 2020-09-13
*   Minor autofan changes (changed type of messages to error instead warning when reboot action required)
*   Improved DoH support (added `dnscrypt` tool)
*   SRBMiner v0.5.1 (added support new algos: argon2id_chukwa, argon2d_dynamic, cryptonight_ccx, cryptonight_xhv, cryptonight_gpu,
cryptonight_upx, cryptonight_heavyx, verushash; added GPU auto tune functionality; other improvements and bug fixes)
*   CCminer-X11k v2.3.2 (fork with X11K support)
*   Bminer: fixed stats for rigs with iGPU

##### 0.6-157@200908 2020-09-08
*   Improved `amd-info` tool (pretty GPU names output, added VRAM info: total/used/free)
*   TeamRedMiner v0.7.10 (added MTP for Navi GPUs, added ethash forced initial allocated epoch --eth_alloc_epoch=N ; added ethash family DAG build slowdown configuration --eth_dag_slowdown=N, default value 4; for eth+zil or Nicehash mining try using --eth_dag_slowdown=9)
*   Fixed stats on some miners (NanoMiner, Bminer)

##### LINUX IMAGE RELEASE 0.6-156 2020-09-05
*   Hive Linux client: v0.6-156@200904
*   Universal boot mode: BIOS | UEFI
*   Linux kernel: v5.0.21-200905-hiveos
*   Drivers version: AMD v19.20, Nvidia: v440.100
*   Supported up to 32 GPU by X.org server
*   OpenVPN updated to v2.4.9
*   ShellInABox updated to v2.21

##### 0.6-156@200904 2020-09-04
*   Improved third-party hardware support (added new CoolBox fan controller)
*   Improved OC applying procedure after `hello` command
*   Fixed `agent` behavior on change rig password
*   CryptoDredge v0.25.1 (fixed high CPU usage on MTP when 'Received new job', improved MTP and Argon2d-NIM algorithms, Allow floating-point intensity, removed obsolete algorithms, bug fixes)
*   T-Rex v0.16.2 (bug fixes: 'can't init enumerate, code -6' error when applying memory tweaks to P102/104/106 cards, memory tweaks stuck after the miner termination, memory tweaks becoming inactive in case of network issues or overclock adjustments)
*   Gminer v2.22 (added 3GB solver for BeamHashIII)
*   miniZ v1.6v6 (improved stability in all algorithms, fixed invalid shares while mining BEAM, smarter check for ssl/tls mining, other minor bug fixes)
*   Update XMRig-CUDA plugin to v6.3.2 (fixed broken AstroBWT)

##### 0.6-155@200828 2020-08-28
*   Improved software watchdog (improved lost GPU detection, improved error messages)
*   Improved `gpu-detect` tool (AMD GPU memory size reading improvement on newer Linux kernels and AMD drivers)
*   XMRig v6.3.3 (improved CUDA loader error reporting and fixed plugin load, bug fixes)
*   XMRig-Klaro v5.6.0 (based on original code XMRig v5.6.0 to mine KLARO coin on RandomXHPFI; select fork 'klaro' under 'xmrig-new')

##### 0.6-154@200825 2020-08-25
*   Fixed `amdmeminfo` tool (fixed trimming BIOS info message on some custom BIOSes)
*   Added CUDA 11.0 RTL (supported by new builds of some miners on 450.x series Nvidia drivers)

##### 0.6-153@200821 2020-08-21
*   Fixed `nvidia-driver-update` tool (fixed start with empty cmd line)
*   NanoMiner v1.10.1 (Nvidia KawPoW (Ravencoin) improvements: better hashrate, less memory consumption)
*   lolMiner v1.07 (added support for mining Cuckoo 29 (Aeternity - use C29AE) on 6G+ cards, added support ItaloCoin hardfork for mining on Cuckaroo 29-48 (cuckaroo29i) on 6G+ cards, minor cosmetic fixes)
*   XMRig v6.3.2 Release (more robust 1 GB pages handling: don't allocate 1 GB per thread if 1 GB is the default huge page size, try to allocate scratchpad from dataset's 1 GB huge pages, if normal huge pages are not available, correctly initialize RandomX cache if 1 GB pages fail to allocate on a first NUMA node)
*   XMRig-CUDA plugin updated to v6.3.1 for all XMRig v6.3.X packages (fixed RandomX regression since v6.2.1)

##### 0.6-152@200819 2020-08-19
*   Improved `nvidia-driver-update` tool (added -f | --force option to bypass some DKMS build errors during install; Tesla driver can be installed by providing appropriate version, ie 440.95.01)
*   Fixed GPU stats for motherboards with some AMD iGPU (i.e. AMD "Wani")
*   Fixed autofan for critical temp and action (minimal critical temp can be set as target+10° vs 20° as was before; in some rare cases mining was not resumed after stop on critical temp)
*   Improved `amdmeminfo` tool (improved Navi support; fixed BIOS version detection on some brands i.e. MSI, Gigabyte; speed up to 10x on some systems; bugfixes and stability improvements)
*   T-Rex v0.16.1 (add memory tweaks for GDDR5 and GDDR5X cards on Pascal 10xx cards, faster DAG generation on kawpow and progpow)
*   Bminer v16.3.0 (support 6G cards for the Cuckatoo32, initial support for ETH mining on AMD Navi, fix compatibility issues when mining ETH on 4G cards)
*   XMRigCC v2.8.0 as XMRig for CPU fork (integrated Randomx variant "Panthera" used by Scala[XLA] algo)

##### 0.6-151@200812 2020-08-12
*   Added support for yet another Chinese variant of AMD RX580 2048SP seen as Ninja brand (updated: amdmeminfo, amdmemtweak. Work on images with amdgpu-pro driver v19.30+)
*   Updated AMD vBIOS Flasher (amdvbflash v4.71: added Navi22 support)
*   Minor fix for `gpu-fans-find` tool (fixed work with AMD Navi)
*   Minor fix for `autofan` (autofan doesn't work correctly with min fan speed set to 1%)
*   Minor AMD OC fix (OC for AMD Vega doesn't work correctly on low GPU core freq)
*   **Gminer v2.21** (major performance improvement for BeamHashIII)

##### 0.6-150@200808 2020-08-08
*   **NanoMiner v1.10.0** (added support KawPow for Nvidia cards)
*   **lolMiner v1.06** (added support for mining BitTube - Cuckaroo-29B and Swap - Cuckaroo-29S, improved Beam stratum, bug fixes)

##### 0.6-150@200806 2020-08-06
*   **XMRig v6.3.2-dev** (added for test; some improvements for 1Gb Huge Pages)
*   **CryptoDredge v0.24.0** (improved argon2d (NIM) algorithm; added '--recompute' option to set memory reduction factor; fixed high CPU usage on MTP-like, Argon2-like and CryptoNight-like algorithms; slightly improved Chukwa (Argon2-512) and Ninja (Argon2-256) algorithms; fixed CryptoNightHaven issue related to 'Unsupported blob size'; new CryptoNightTLO algorithm; new sha256csm algorithm; other minor fixes)
*    **lolMiner v1.05** (improved performance of BeamHashIII for all supported 4G and higher cards by 4-8% depending on model; fixed C29M, other bug fixes)

##### 0.6-150@200801 2020-08-01
*   **XMRig v6.3.1** (added command line options '--randomx-cache-qos' and '--argon2-impl')
*   **TeamRedMiner v0.7.9** (fixes for mixed OpenCL rigs, added '--eth_epoch' argument for easier epoch testing; added '--eth_aggr_mode' for automatic aggressive 'B' mode on Polaris 8GB gpus; added '--watchdog_disable' argument)

##### 0.6-150@200729 2020-07-29
*   Improved Autofan module (added as a secondary target temperature Tmem for AMD Vega and Navi GPUs; added a new mode "Smart Mode")
*   Updated some system libs
*   **Bminer v16.2.12** (improved Cuckaroo29z performance)

##### 0.6-149@200723 2020-07-23
*   **Gminer v2.20** (improved Cuckarooz29 algorithm on RTX cards)
*   **PhoenixMiner v5.1c** (added more Pascal-based Nvidia cards to the list of supported Nvidia cards for memory timings; added new parameter '-nvmem' to force using straps even on unsupported Nvidia GPUs: use '-nvmem 1' for GDDR5 cards, or '-nvmem 2' for GDDR5X cards; removed some dead ethash-based altcoins and updated the support for the rest of them; other small fixes)

##### 0.6-149@200722 2020-07-22
*   Improved autofan module (reworked AMD fan control)
*   Fixed applying pill on some early GTX 1080 (implemented a special Nvidia pill applying procedure for some early versions of GTX 1080 PCBs)
*   Bminer v16.2.11 (improved performance of the Cuckaroo29z, more fixes on fidelity issues on GRIN)
*   miniZ v1.6v5 (fixed some issues of previous version)

##### 0.6-148@200721 2020-07-21
*   Improved network stability
*   **Bminer v16.2.10** (improved Cuckarooz29 algorithm; fixed fidelity issues for GRIN)
*   **miniZ v1.6v4** (structural software improvements: size < 16Mb; speed improvements for BeamHashIII; fixed invalid shares on AION/F2Pool; faster feedback on miniZ start; fixed some more stability issues that caused unusual random crashes)
*   **TeamRedMiner v0.7.8.1** test (added support mixed AMD OpenCL platforms: legacy and pal)
*   **T-Rex v0.15.9** test (added memory tweaks for GDDR5 and GDDR5X 10xx series cards)

##### 0.6-147@200720 2020-07-20
*   **TeamRedMiner v0.7.8** (ready for upcoming XHV/Haven Protocol hardfork on July 20, 2020; tiny Nimiq optimizations: 1-2% max, mostly Vega and Navi; some bugs fixed)

##### 0.6-147@200719 2020-07-19
*   **Bminer v16.2.9** (improved Cuckarooz29 algorithm)

##### 0.6-147@200718 2020-07-18
*   Minor fix related to GPU stats
*   **Gminer v2.19** (improved Cuckarooz29 algorithm)

##### 0.6-146@200716 2020-07-16
*   **PhoenixMiner v5.1b** (added support for VRAM timing adjustments for Nvidia cards of 10x0 series: new command-line parameters '-straps', '-vmt1', '-vmt2', '-vmt3', and '-vmr'; added -ttli option to automatically decrease the mining speed to avoid overheating the GPUs over the target temperature; many other small improvements and fixes)
*   **Gminer v2.18** (added Cuckarooz29 algorithm)
*   **Bminer v16.2.8** (added support Cuckaroo29z algorithm for the GRIN hardfork, various performance improvements on the AMD cards on Ethash)
*   **XMRig v6.3.0 + CUDA plugin v6.3.0** (added support for upcoming Haven offshore fork; RandomX: added new option 'cache_qos' in randomx object for cache QoS support; CryptoNight OpenCL: fix for long input data)
*   **NanoMiner v1.9.6** (XMR mining: fixed miner termination in case there are no jobs for 10 minutes)

##### LINUX IMAGE RELEASE 0.6-146 2020-07-14
*   Hive Linux client: v0.6-146@200714 (stable branch based on Ubuntu 18.04)
*   Universal boot mode: BIOS | UEFI
*   Linux kernel: v5.0.21
*   Drivers version: AMD v19.20, Nvidia: v430.64
*   Supports Nvidia GPUs: 10xx/16xx/20xx series, AMD GPUs: Polaris and Vega families

##### 0.6-146@200714 2020-07-14
*   Autofan: fixes & improvements (auto switching to manual control on AMD GPUs, more precise and faster AMD fan control, human readable payload in error msgs)
*   **lolMiner v1.04** (slightly improved performance (2-5%) on all AMD cards on BeamHashIII, most significant (about 7%) on Navi GPUs)
*   **Gminer v2.16** (added support hardfork TUBE/BitTube to Cuckaroo29b on AMD cards)

##### 0.6-145@200711 2020-07-11
*   **XMRig v6.2.3** (AstroBWT: fixed OpenCL compilation on some systems; KawPow: optimized CPU share verification, fixed DAG initialization on slower AMD GPUs, fixed rare duplicate share errors; RandomX: added error message when MSR mod fails, small speedup on Ryzen CPUs; fixed GPU health readings for pre Vega GPUs; added results and connection reports)

##### 0.6-145@200708 2020-07-08
*   **Gminer v2.15** (added Cuckaroo29b algorithm for TUBE/BitTube hardfork on NVidia GPUs)
*   **Bminer v16.2.7** (improved performance for the BeamHashIII, fix compatibility issues with Beam mining pools, reduced rejection rates for all miners)

##### 0.6-145@200706 2020-07-06
*   **Gminer v2.14** (fixed bug with share difficulty on cuckaroom29-qitmeer algorithm, lowered devfee to 3% on cuckaroom29-qitmeer algorithm)

##### 0.6-145@200705 2020-07-05
*   **Gminer v2.13** (added support Qitmeer hardfork to cuckaroom29 algorithm)
*   **lolMiner v1.03** (added new BeamHashIII 4G solver, replaces the 6G solver on AMD Vega GPUs and earlier: +5-8% performance on RX 580 & Vega GPUs, added new BeamHashIII 6G solver on ROCm and for AMD Navi GPUs: +8-10% performance on Navi cards)

##### 0.6-145@200702 2020-07-02
*   **Gminer v2.12** (improved performance for BeamHashIII 2%-10% dependent from GPUs, removed auto-switching to BeamHashIII)
*   **NoncerPro Nimiq CUDA v3.3.1** (added '--extra', '-x' option for solo mining on icemining pool, eg: usage : -x="m=solo")
*   **WildRig-Multi v0.25.2** (fixed crash after devfee for progpow variants, fixed wrong logic for temp limits which was broken since version 0.25.0, initial support for AMD hardware monitoring)

##### 0.6-145@200701 2020-07-01
*   Fixed some issues with hardware watchdog (watchdog stopped working after the boot in some cases)
*   **lolMiner v1.02** (disabled BeamHashIII auto switcher, fixed a bug that made the miner not start mining Cortex, fixed a bug that made the miner not starting 'BEAM-III' on RX 550 4G GPUs, fixed a bug with BeamHashI 3G solver)
*   **nq-miner v0.99.7** (added support Icemining solo mode: '-pool-params m=solo')
*   ***NEW*** **XPM miner by eXtremal-ik7 OpenCL v10.5-beta1 & CUDA v10.3** (XPM/PrimeCoin miners for OpenCL/CUDA)

##### 0.6-144@200629 2020-06-29
*   **Bminer v16.2.5** (improved performance of the BeamHash III miner, fixed critical issues that the BeamHash III miner computes invalid solutions, reduced the rejection rates of the Ethereum and ProgPOW miners)
*   **miniZ v1.6v3** (removed autoswitch for Beam, fixed --pers auto that was not working on NiceHash, added support for GTX 1650 4GB, in BeamHashIII, added a few corrections to 144,5 that possible will reduce cpu usage)
*   **Beam OpenCL v1.0.85** (open-source miner from Beam devs with 0% devfee updated for BeamHashIII, miner slow but it's free)

##### 0.6-144@200628 2020-06-28
*   **T-Rex v0.15.8** (added extranonce support for Nicehash)
*   **miniZ v1.6v2** (added support for BeamHashIII - 144,5s; completely reworked the --ocX mechanism; changed kernel calls for 150,5 possible improves CPU usage; better default kernels for GTX1070, on stock settings, for all algorithms; fixed --show-mode option that was only showing in combination with other options)
*   **Gminer v2.11** (added support BeamHashIII algorithm for Nvidia GPUs; improved Cuckatoo32 performance up to 5%-8% dependent on GPU; lowered fee for Cuckatoo32 algorithm to 2%)
*   **lolMiner v1.01** (***Changes v1.01 vs v1.0***: improved performance of BeamHashIII on all 6G+ cards ~4-5%; added 3G* / 4G solver for BeamHashIII; fixed an issue with mining BeamHashIII to NiceHash; --tls now allowed to be used multiple times to configure it for each pool seperately. ***Changes v1.0 vs v0.9.8***: added optimizes solvers for BeamHashIII for AMD & Nvidia GPUs - BEAM for autoswitch on 8G cards or BEAM-III for manual switch on 6G cards; improved up to +10% performance on GRIN-C29M solver for 8G GPUs; added Cuckaroo-30 solver to mine Cortex; AMD Navi does now work on all supported algorithms; added support for non-integer difficulty on Grin; reactivated support for BeamHashI including support for personalization strings; removed support mining MNX due dead project; Note: this version has new config format - versions prior v1.0 no longer supported.)
*   **TeamRedMiner v0.7.7** (added support for Nimiq Navi; added support for Icemining Nimiq solo mining mode)

##### 0.6-144@200625 2020-06-25
*   **Bminer v16.2.4** (fixed the miscalculations of the targets for Qitmeer)

##### 0.6-144@200624 2020-06-24
*   **Bminer v16.2.3** (added support the Cuckaroo29m hardfork for Qitmeer, fixed compatibility issues when mining Ethereum on Nicehash, removed CKB support)
*   **NBMiner v31.1** (added cuckatoo32 for GRIN on Nvidia 8G above GPUs, kawpow now fully supports NiceHash's protocol)

##### 0.6-144@200623 2020-06-23
*   **TeamRedMiner v0.7.6.4** (integrated Nimiq node.js network proxy into the miner, fixed Nimiq bug that could lose shares, especially against lower vardiff pools, fixed Nimiq bug that could cause duplicate shares on startup for low-diff pools, fixed regression bug for ethash Nicehash, correct stratum mode now used again)
*   **XMRig v6.2.2** (fixed detection of AVX2/AVX512, AMD GPUs health display fixed, improved displaying information for compute errors on GPUs, fixed NiceHash disconnects for KawPow; updated CUDA plugin to 6.2.1: optimized KawPow, about 2% hashrate improvement, 10% faster DAG initialization; added fast job switching for KawPow, almost zero stale shares; *Notes: switched this branch and version to Latest*)
*   **HellMiner v0.52 for VerusHash 2.2** (slightly faster, added new thread priority option)
*   **XMRig v5.11.4** (Latest v5.x series: fixed detection of AVX2/AVX512, AMD GPUs health display fixed, updated CUDA plugin to 6.2.1)
*   **NEW** **QuarkChain OneButton EthMiner v2.0** (QuarkChain mainnet Node/Cluster miner)

##### 0.6-144@200619 2020-06-19
*   **CPUminer-Opt-JayDDee v3.14.3** (fixed hodl algo potential memory alignment issue)
*   **XLArig v5.1.0** (xmrig-new fork; sync codebase to XMRig v5.11.1; implemented Panthera Algorithm for v7 network)
*   **TeamRedMiner v0.7.6.2** (added beta support for Nimiq via wss proxy to mine in dumb mode; public nimiq proxy at 18.196.209.223:4444 to nimiq.icemining.ca)
*   **Bminer v16.2.2** (improved the performance of Ethereum mining on AMD GPUs, improved stability of the Cuckatoo32 miner, added support automatic transition to BeamHashIII, removed ZEC miner support)
*   **miniZ v1.5u2** (fixed bug that on ZEL mining was not submitting shares on some pools, adjusted default kernels for GTX1070, on stock settings, for all algorithms)

##### 0.6-144@200616 2020-06-16
*   **NHEqMiner VerusHash v0.8.2** (improved miner performance; Note: AVX2 capable CPU needed)
*   **XMRigCC v2.7.0** (fork of old XMRig for CPU; integrated chukwa variants algos pengo for pengolincoin and ninja for ninjacoin)
*   **SRBMiner-Multi v0.4.7** (removed devfee for 'blake2s', 'mtp', 'keccak', 'yespoweritc', 'm7mv2', 'cryptonight_catalans', 'cryptonight_talleo' algorithms; lowered 'bl2bsha3' devfee to 0.85%; fixed 'randomx' algorithm when running on 64+ threads)
*   **miniZ v1.5u** (major hashrate improvements on 144/5 up to 6.5%; minor hashrate improvements on 125/4 up to 1%; fixed connection latency issues; added --ocX option for automatic tunning of the best kernel; added --show-mode option to show miniZ kernel that each GPU is using; reduced memory utilization on 144/5 for all GPUs; reduced memory usage on 3GB GPUs for 125/4)
*   **TeamRedMiner v0.7.6** (added support Navi14 RX 5500XT, fixed broken keyboard input in screen and tmux sessions affected to miner command, fixed watchdog support for hard driver crashes, fixed kawpow NH extranonce support)

##### 0.6-144@200614 2020-06-14
*   NHEqMiner VerusHash v0.8.1 (updated to upcoming hardfork VerusCoin to VerusHash v2.2 PoW)
*   HellMiner v0.5 for VerusHash v2.2 (updated to upcoming hardfork VerusCoin to VerusHash v2.2 PoW)
*   CPUminer-Opt-rplant v4.5.11 (added curvehash algo, oblivion coin)

##### 0.6-144@200610 2020-06-10
*   XMRig v5.11.3 stable + CUDA plugin 6.2.0 (small fixes, new CUDA plugin)
*   XMRig v6.2.0 beta + CUDA plugin 6.2.0 (added new algorithm cn/ccx for Conceal; Note: this version marked as Beta and added for testing purposes, please select version from miner configuration)
*   WildRig-Multi v0.25.1 (adl/nvml now won't initialize if not needed, option '--opencl-platforms' now can be set with values 'amd' and 'nvidia', fixed possible crash after donation mining on progpow variants, improved lyra2 variants for nvidia)
*   PhoenixMiner v5.0e (added additional fixes and some workarounds for the ETH to ETC switching problem)
*   CPUminer-Opt-rplant v4.5.10 (added 'hodl' algo, lyra2z330 improvements)
*   Gminer v2.10 (major performance improvements for qitmeer up to +20%, fixed compatibility with latest nvidia drivers known as "no device found" error)

##### 0.6-144@200607 2020-06-07
*   XMRig v6.0.1 beta (replaced previous package v6.0.0, minimal CUDA plugin v6.1.0; Note: this version marked as Beta and added for testing purposes, please select version from miner configuration)
*   WildRig-Multi v0.25.0 (slightly improved speed of kawpow/progpow, bug fixes for progpow variants, initial support NVIDIA GPUs via OpenCL and PTX ISA)
*   PhoenixMiner v5.0d (fixed problem with crashing or slowing down when switching from ETC to ETH mining)

##### 0.6-144@200606 2020-06-06
*   Improved `agent`
*   XMRig v6.0.0 beta + CUDA plugin v6.1.0 (added support kawpow, removed support cn-gpu, improved hashrate up to x3 on CUDA AstroBWT; *Note: this version marked as Beta and added for testing purposes, please select version from miner configuration*) 
*   SRBMiner-Multi v0.4.6 (fixed 'defyx' algorithm on Intel CPU's)
*   TeamRedMiner v0.7.5 (increased `ethash` support on 4GB GPUs up to epoch 380-383, implemented split ethash dag buffers for 8GB GPUs to support DAGs over 4GB, `kawpow` optimizations: Navi +2.25%, Vega +1.25%, Polaris +0.25%)

##### 0.6-143@200603 2020-06-03
*   Improved pci.ids updating (rework from updating via internet to Hive opt package)
*   Fixed bug with checking VBIOS size (so 1 MB VBIOS can be flashed) 
*   Improved/fixed hashrate watchdog (fixed starting after miner installation completion, fixed checking for non-zero hashrate in Algo mode)
*   CPUminer-Opt-JayDDee v3.14.2 (optimize log output)
*   lolMiner v1.0 alpha 2 (new GRIN-C29M code: +10% speed on most supported cards, improved GRIN-C29M fidelity which gives additionally 2-3% better pool hash; *Note: this version replaces v1.0 alpha 1 and marked as Preview and added for testing purposes, please select version v1.0 from miner configuration*)
*   SRBMiner-Multi v0.4.5 (added 'randomepic' algo, improved up to 1,5% hashrate on Vega, improved RandomX and many other improvements and bug fixes)
*   NanoMiner v1.9.5 (fixed 4 GB Ethash DAG problem for AMD GPUs)
*   PhoenixMiner v5.0c (added SO_REUSEPORT option on to prevent problems when the miner is restarting)

##### 0.6-142@200528 2020-05-28
*   Improved `hive-replace` (now can be runned from local console if GUI disabled)
*   TeamRedMiner v0.7.3 (fixed mining on Vegas on older amdgpu-pro drivers; emergency patch for 4GB cards to handle a few more ETC epochs; added watchdog script)
*   PhoenixMiner: latest switched to v5.0b from 4.9c

##### 0.6-141@200524 2020-05-24
*   Improved `hive-replace` (added support for Ubuntu 14 based OS)
*   Sync changes AMD OC with new web form (fixed VDDCI, MVDD for Navi, added support PL for Vega and Navi)
*   CPUminer-Opt-JayDDee v3.14.1 (some changes related to solo mining)
*   XMRig (new) v5.11.2 (improved JSON config error reporting, optimized RandomX dataset initialization)
*   PhoenixMiner v5.0b (added support for mining with 4 GB AMD cards beyond the DAG epoch 350, up to 380; added support latest drivers. *Note: this version marked as Beta and added for testing purposes, please select version from miner configuration*)
*   T-Rex v0.15.7 (reduced share rejects especially on high intensity and low difficulty)

##### 0.6-140@200519 2020-05-19
*   Minor system changes
*   Z-Enemy (ccminer-enemy) v2.6.2 (fixed compatibility with NH, MPH and some other pools, fixed start on Ubuntu 16 based distro using json config file)
*   WildRig-Multi v0.24.1 (added parameter --progpow-kernel, speedup ProgPow/KawPow up to 10% on pre-Navi GPU's)
*   DamoMiner v2.7.8 (added support AMD cards on RVN)
*   NanoMiner v1.9.4 (fixed setting up email for RVN, fixed incompatibility issue with some Ethereum pools)
*   TeamRedMiner v0.7.1 (added 'kawpow' algo for RVN, added AMD RX5700 support on 'ethash' and 'kawpow'; other improvements)
*   CPUminer-Opt-JayDDee v3.13.1.1 (minor update)

##### 0.6-139@200514 2020-05-14
*   Small system changes (improved support for third-party hardware; better CUDA RTL handling with installed Nvidia drivers)
*   Ethminer v0.19.0-2 (eliminated 4GB DAG limit on OpenCL, small speedup on OpenCL)
*   CPUminer-Opt-JayDDee v3.13.1 (added 'minotaur' algo for Ringcoin)
*   WildRig-Multi v0.23.2 (faster kernel compilation for ProgPow/KawPow)
*   KawPowMiner (ethminer-kawpowminer) v1.2.3 (improved reconnection, added miner version to mining.subscribe)
*   NanoMiner v1.9.3 (KawPow: performance improved on AMD Navi GPUs, +16% on stock RX 5700 XT and +14% on stock RX 5700; average performance was slightly improved for pre-Navi AMD GPUs)
*   miniZ v1.5t3 (125,4 (ZEL): major improvements for various GPUs. Up to ~11% for 1660ti and ~8% for RTX 2070; 150,5,3 (BEAM): major improvements up to ~3-4% for GTX 1660 Ti, RTX 2070. Minor for other GPUs)
*   Z-Enemy (ccminer-enemy) v2.6.1 (KawPow changes: faster initialization on multi-gpu rigs, performance improvements, smoother gpu/power load)

##### 0.6-138@200510 2020-05-10
*   Update Intel's e1000 series LAN card driver installation script (set default version to latest v3.8.4)
*   T-Rex v0.15.6 (bug fixes: DAG regeneration on epoch change, benchmark for 'kawpow')
*   SRBMiner-Multi v0.4.4 (added 'ethash' and 'ubqhash' algos)
*   DamoMiner v2.7.5 (fixed issues on some pools)
*   WildRig-Multi v0.23.1 (added 'kawpow' and progpow variants 'ethercore', 'sero', 'zano')

##### 0.6-137@200508 2020-05-08
*   TT-Miner v5.0.1 (fixed a 'duplicate share issue' that could happened on all ProgPoW like algos; starting from v5.0 devfee free version)
*   Bminer v16.2.1 (fixed compatibility issues with some Raven mining pools)
*   T-Rex v0.15.5 (less memory consumption. Possible crash fix for "out of memory" error for GPUs with 3GB; unblocked feature of intensity setting)
*   NanoMiner v1.9.2 (fixed possible wrong GPU hanging detection in some network failure scenarios; fixed confusing common options set up in config)
*   XMR-Stak-RX (xmr-stak-randomx) v1.0.5 (added support mining 'keva' with alias 'randomx_keva' and 'safex' with alias 'randomx_safex')
*   CPUminer-Opt-JayDDee v3.13.0.1 (fixed xevan AVX2 invalid shares)

##### 0.6-137@200506 2020-05-06
*   Fixed issue with wrong symlink in CUDA RTL
*   NanoMiner v1.9.1 (fixed issue with bsod.pw RVN testnet pool)
*   NBMiner v30.2 (fixed `kawpow` duplicate share issue on some pools)
*   T-Rex v0.15.4 (fixed showing miner version info for mining pool)
*   Bminer v16.2.0 (improved performance on mining AE and BFC; added support for mining SERO and RVN)
*   Z-Enemy (ccminer-enemy) v2.5 (added 'kawpow' algo; builds with CUDA 9.2/10.0/10.1 available, default 10.0)
*   ***NEW*** HellMiner v2.1 (VerusCoin CPU miner)
*   Fixed config generation in XMRig (old) / XMRig-AMD / XMRig-Nvidia / XMRig (new) (field 'rig-id' which used on some pools not filled with worker name)

##### 0.6-136@200504 2020-05-04
*   Updated some system tools
*   T-Rex v0.15.3 (added 3 new algorithms: 'kawpow', 'progpow', 'mtp-tcr'; improved stat table: added output percentage of rejected shares) 
*   NBMiner v30.1 (reduced startup time on 'ethash' and 'kawpow'; memory tweak don't apply if 0 set on corresponding GPU; fixed a possible crash on certain rigs of reason 'invalid kernel image'; printed system information on start)
*   NanoMiner v1.9.0 (added 'kawpow' algo for upcoming RVN hardfork implemented on AMD GPUs)
*   KawPowMiner v1.2.2 (allowed full port range)

##### 0.6-135@200502 2020-05-02
*   T-Rex v0.15.2 test (fixed all known bugs v0.15,0/v0.15.1; *Note: this version for testing purposes, please select version from miner configuration*)
*   TT-Miner v4.0.3 (fixed command line parameter bug)
*   KawPoWMiner v1.2.1 (added more extranonce validation; *Note: to use the miner, please select the `kawpowminer` fork in the`ethminer` configuration settings*)

##### 0.6-135@200501 2020-05-01
*   T-Rex v0.15.1 test (fixed "unspecified launch failure" error when mining kawpow; *Note: this version for testing purposes, please select version from miner configuration*) 
*   NBMiner v30.0 (added `memory-tweak` option for using optimized timings on Nvidia GPUs with GDDR5/5X memory, the option can take values from 1 to 6 to activate, add `"memory-tweak": "MODE"` to the configuration with this option using pill for GDDR5X not necessary; added `verbose` option for debugging communication with the pool; added number of shares per GPU in both log print and API)
*   DamoMiner v2.6.9 (improved kawpow hashrate)
*   ***NEW*** KawPoWMiner v1.2.0 (Ravencoin KawPow open source miner with 0% devfee for AMD and Nvidia GPUs; *Note: to use the miner, please select the `kawpowminer` fork in the`ethminer` configuration settings*)

##### 0.6-135@200428 2020-04-28
*   Updated CUDA libs (added CUDA 10.2 RTL)
*   T-Rex v0.15.0 test (added 3 new algorithms: kawpow, progpow, mtp-tcr; improved stat table: added output percentage of rejected shares; *Note: this version for testing purposes, please select version from miner configuration*)
*   Gminer v2.09 (improved cuckatoo32 performance with up to +20% dependent on GPU and OC mode)
*   XMRig v5.11.1 (up to 1% RandomX perfomance improvement on recent AMD CPUs; fixed possible double connection to a pool)
*   CPUminer-Opt-JayDDee v3.12.8.2 (fixed x12 AVX2 rejects, fixed phi AVX2 crash)
*   TT-Miner config generation updated for v4.x and CUDA 10.2
*   DamoMiner: fixed config generation if Extra config arguments present

##### 0.6-134@200422 2020-04-22
*   TT-Miner v4.0.1 (added support 'kawpow' for upcoming RVN/Ravencoin hardfork, added support mining Hanacoin, EtherCore, TecraCoin (MTP), Veil (ProgPoW testnet), improved algo structure with general performance improvements on all algos)
*   DamoMiner v2.6.6 (added support 'kawpow' for upcoming hardfork RVN/Ravencoin)

##### 0.6-134@200421-2 2020-04-21
*   fixed broken execution commands from dashboard

##### 0.6-133@200421 2020-04-21
*   Improved configs sync 
*   Updated AMD BIOS flasher with Navi support (Notes: 1Mb ROM not supported yet)
*   CCminer-djm34 v1.3.2 (fixed high CPU usage on MTP algo) 
*   CPUminer-Opt-JayDDee v3.12.8.1 (fixed yescryptr8g invalid shares) 
*   lolMiner v1.0 alpha 1 preview (added cuckaroo30 for mining CTXC/Cortex, added temperature, fan speed and consumption readings. Notes: if you want try this version select it from miner config options) 
*   XMRig-MO v5.11.0 (MoneroOcean release)
*   NEW EtherCoreMiner v1.0.0 (etherminer fork 'ethercore') 
*   NEW DamoMiner v2.6.3 (GPU miner for ETH and dual mode ETH + CKB/HNS/TRB)

##### 0.6-132@200414 2020-04-14
*   Bminer v16.1.1 (improved the performance of Cuckaroo29m, added support mining Qitmeer)
*   XMRig v5.11.0 (added support AstroBWT CUDA and OCL for NVIDIA GPUs, some RandomX optimizations)

##### 0.6-132@200411 2020-04-11
*   SRBMiner-Multi v0.4.3 (added 'tellor' algo, improved 'minotaur' algo)

##### 0.6-132@200410 2020-04-10
*   CPUminer-opt-JayDDee v3.12.8 (optimization for 'yespower' algo, rewrote diff conversion functions from scratch, some code cleanup and assorted small changes)
*   NBMiner v29.1 (fixed low hashrate of 'kawpow' on AMD Navi GPUs, improved 'kawpow' hashrate on AMD GPUs)

##### 0.6-131@200404 2020-04-04
*   SRBMiner-Multi v0.4.2 (improved 'cryptonight_bbc' on 4G Ellesmere cards, small improvements on 'yespower' CPU algo, fixed 'handshake' mining on Nicehash)
*   Gminer v2.06 (improved miner stability on qitmeer)

##### 0.6-131@200403 2020-04-03
*   NBMiner v29.0 (added support for RVN new algo 'kawpow' mining on Nvidia & AMD GPUs)
*   Gminer v2.05 (improved performance up to +30% for qitmeer, significantly decreased CPU usage for qitmeer)
*   RHminer v2.3 (improved network stability and improved hashrate by 5-10% depending CPU and memory speed)

##### 0.6-131@200401 2020-04-01
*   Folding@Home client v7.5.1 (if you used custom version before then all your data will be safe)
*   Bminer v16.1.0 (fixed fidelity issues on Cuckatoo29m, support for BFC and Cuckatoo32, improved stability of ETH mining)

##### 0.6-131@200330 2020-03-30
*   NBMiner v28.1 (added support HNS & HNS+ETH mining on NiceHash)
*   Gminer v2.04 (added KawPoW algorithm for upcoming Ravencoin hardfork, added "--trim" parameter to control additional trim round count for cuckoo24 (qitmeer) algorithm, this options will help reduce cpu load)

##### 0.6-131@200328 2020-03-28
*   Fixed potential bug with miner starting (miner doesn't start with the same FS when Rocket button used)
*   Updated `amdmeminfo` tool (added detection Samsung K4G80325FC GDDR5 memory)
*   NBMiner v28.0 (added support for mining TRB & TRB+ETH on Nvidia GPUs, added support for mining ETH on MiningRigRentals service, minor improvements and fixes)
*   WildRig-Multi v0.20.5.3 (fixed rejects on x17r when haval is first in hashorder, fixed low difficulty shares on 666pool, implemented x17r-protocol2 to support other pools)
*   XMRig-Epic v5.5.3/v0.0.1 (EpicCash v0.0.1 mining client based on XMRig v5.5.3 code for RandomX PoW, fork work only with 51pool.online pool)

##### 0.6-130@200325 2020-03-25
*   Minor OS improvement (`hello` & `agent` - don't restart miner if the flightsheet not changed)
*   SRBMiner-Multi v0.4.1 (added CPU algorithm 'minotaur', added CPU algorithm 'yespowerres', improved up to 2-4% on 'cryptonight_bbc' on some GPU's)
*   WildRig-Multi v0.20.5.1 (enabled all algorithms for Navi, added lyra2tdc, added x17r algorithm for ufo-project)

##### 0.6-129@200323 2020-03-23
*   Minor fixes for `net-test`
*   Fixed memory vendor displaying for AMD Vega10/Vega20 family GPUs
*   Gminer v2.03 (added qitmeer support)
*   XMRig (unified) v5.10.0 (added AMD GPUs support for AstroBWT algo, added AVX2 optimized code for AstroBWT algo)
*   CPUminer-Opt-JayDDee v3.12.7 (fixed a file descriptor leak which caused the CPU temperature and frequency query to report zeros, stale share reduction for yescrypt and sonoa)
*   Ethminer v0.19.0-beta.1 (new build: more accurate checks for available memory; fast share evaluation from previous job after DAG switch; reusing DAG buffer in OpenCL mode and others)
*   Nanominer: fixed stats for RandomX algo

##### 0.6-128@200315 2020-03-15
*   Gminer v2.01 (updated BBC algorithm to support latest hardfork, improved ProgPoW support)
*   NBMiner v27.7 (improved HNS & HNS+ETH on Nvidia GPUs, fixed ETH mining on NiceHash, fixed NVML initialization failure on certain cases)
*   SRBMiner: fixed some issues with miner restart after fault and log file rotation

##### 0.6-127@200310 2020-03-10
*   XMRig (unified) v5.9.0 + CUDA plugin v2.2.0 (added new RandomKEVA algorithm for upcoming Kevacoin fork, fixed invalid AstroBWT hashes after algorithm switching)
*   SRBminer-Multi v0.4.0 (added algorithm 'randomkeva', added Navi support for 'cryptonight_bbc')
*   NoncerPro Nimiq CUDA miner v3.3.0 (~10% hashrate improvement, added new option --autoOptimize. Set this to false to disable the optimizer auto run)

##### 0.6-126@200308 2020-03-08
*   ETHminer v0.19.0-beta (implemented fix for Nicehash, choose this version manually in miner setting)
*   Gminer v2.00 (added ProgPoW (Sero) solver for Nvidia GPUs)
*   CPUminer-Opt-JayDDee v3.12.6.1 (integrated SSL patch to mainline code; implemented stale share reduction for yespower, x25x, x22i, x21s, x16*, scryptn2)

##### 0.6-126@200307 2020-03-07
*   Fixed `repomirror` (update repo was broken) 
*   NBMiner v27.5 (fixed high ETH reject rate on certain pools when mining HNS+ETH, slightly improved mining HNS+ETH on Nvidia GPUs)
*   CPUminer-Opt-JayDDee v3.12.6 (improved stale share detection for getwork, added highest and lowest accepted share to summary log)
*   XMRig (unified) v5.8.2 (AstroBWT algorithm 20-50% speedup, added new option `astrobwt-max-size`)
*   XMRigCC v2.6.2 (added RandomKEVA, integrated upstream changes from XMRig: integrated AstroBWT, RandomX hashrate improvements, etc ...)
*   Fixed bug in generating configuration for rig-id field on all XMRig miners for all platforms

##### 0.6-125@200304 2020-03-04
*   AMD OC (Polaris) optimizations (OC apply only to GPU with changed settings; added ability to set VDDCI in MDPM field in classic mode)
*   Improved `amd-info` tool (show memory voltage and VDDCI on Polaris and Vega)
*   Fixed switching X server output to connected monitor on Nvidia GPU
*   XMRig (unified) v5.8.1 (added new AstroBWT algorithm for upcoming DERO fork)
*   SRBMiner-Multi v0.3.9 (unofficial yet; this is v0.3.8 build which should now work on older Hive images)
*   miniZ v1.5t2 (improvements for EQ 150/5/3: major (~2-4%) for GTX 1660 Ti, 1080 Ti, and RTX GPUs)

##### 0.6-124@200303 2020-03-03
*   SRBMiner-Multi v0.3.8 (hashrate increased even more on Kadena mining and at the same time lowered power usage, small hashrate increase on 'yescrypt' CPU algo, minor bug fixes)
*   Gminer v1.99 (improved cuckaroom29 performance, improved perforance for handshake algorithm, added Ethash+Handshake dual)
*   NBMiner intensity fix (for v27.3 & v27.4)

##### 0.6-124@200302 2020-03-02
*   SRBMiner-Multi v0.3.7 (huge hashrate improvement on mining KDA/Kadena)
*   NoncerPro Kadena v2.2.0 (added the 5x hashrate improvement for AMD cards, slight hashrate improvement for some Nvidia cards)
*   CPUminer-Opt-JayDDee v3.12.5 (fixed incorrect share diff for stratum and getwork, fixed incorrect target diff for getwork, getwork: reduce stale blocks, faster response to new work)

##### 0.6-124@200301 2020-03-01
*   AMD OC (Polaris) fixes & optimizations (added ability to set VDDCI in MDPM field in aggressive mode; fixed empty OC profile applying in aggressive mode; fixed instability in aggressive mode with DPM 1 on some GPUs; set memory state only if state or clock are specified, except aggressive mode with set core clock and DPM>1 to reduce usage in idle mode)
*   NBMiner v27.4 (added HNS+ETH mining on AMD GPUs, improved HNS+ETH performance on Nvidia GPUs)
*   NoncerPro Kadena v2.1.1 (5x hashrate improvement in solo mode for Nvidia cards, this version doesn't work on AMD cards)
*   CPUminer-Opt by JayDDee v3.12.4.6 (yet another fixes for getwork mode)
*   Fixes for SRBMiner-Multi (some workaround to run v0.3.6, fixed hashrate units in stats)

##### 0.6-123@200226 2020-02-26
*   `For owners of AMD RX 400/500 series cards reboot strongly recommended after update will completed (use 'Reboot after complete' option)`
*   Fixed AMD OC (Polaris) (apply idle power fix only in aggressive mode with core and vddc set)
*   Fixed `amd-info` (incorrect data displaying with amdmemtweak v0.1.9.1 CLI)
*   Updated `amdmeminfo` tool (added detection Hynix H5GC8H24AJR GDDR5 memory chip)
*   Gminer v1.98 (improved handshake performance, lowered devfee to 2% for handshake)
*   CPUminer-opt-jayddee v3.12.4.4 (some issues with getwork/solo mode fixed
*   SRBminer-Multi v0.3.6 (updated cryptonight_bbc algorithm to PoW changes from block 133060)
*   NEW XMRig-RandomEVO v5.6.0 (fork randomevo of XMrig unified to mine EVO/Coinevo coin)

##### 0.6-122@200225 2020-02-25
*   Fixed OC for AMD Polaris (affected to OC profile with empty memory state)
*   XMRig (unified) v5.7.0 (added SOCKS5 proxies support for Tor, fixed duplicate jobs in daemon (solo) mining client, slightly speedup by 0.3-0.4% on RandomX depending on CPU)
*   CPUminer-opt-jayddee v3.12.4.3 (fixed segfault in new block log for getwork)
*   XMRig-BBC (xmrig fork: bigbangcore) v1.3 (improved hash algorithm of CryptoNight-BBC)

##### 0.6-121@200224 2020-02-24
*   X server improvements (added Auto start option by default - X server starts only if Nvidia GPUs are present; fixed X server crashing with lot of AMD GPUs; optimized boot sequence)
*   Improved overclocking for AMD Polaris family cards (much faster and stable aggressive OC. memory clock is always applied in MDPM 1 modereduced power usage in idle mode if DPM or MDPM settings are used)
*   Updated some tools for AMD cards
*   Bminer v16.0.7 (initial support for mining Ethash as well as dual mining Ethash and Handshake on AMD)
*   lolMiner v0.9.8.1 (improved GRIN-C29M up to +7-12% depending on card, added support for AMD 5500/5600 series on all Grin algos, dded BEAM support for for 5500/5600/5700 series)
*   CPUminer-opt-jayddee v3.12.4.2 (improved Lyra2v2 avx2 and avx512, fixes for getwork/solo mode)
*   MBminer: fixed stats for AMD  cards

##### 0.6-120@200220 2020-02-20
*   Minor system fixes
*   NBMiner v27.2 (improve HNS performance on AMD GPUs)
*   NanoMiner v1.8.2 (network stability improved)
*   SRBMiner-Multi v0.3.5 (added 'cryptonight_bbc' algorithm devfee to 2.5%, lowered devfee for 'bl2bsha3' to 2%, added GPU sensors for Linux version and ability to use some related options)

##### 0.6-119@200219 2020-02-19
*   NBMiner v27.1 (improve HNS performance on Nvidia GPUs, added support for HNS mining for AMD GPUs)
*   Gminer v1.97 (added Cuckatoo32 and Handshake solvers)
*   CPUminer-opt-rplant v4.5.5 (fixed broken yespower and yespowerR16)

##### 0.6-119@200218 2020-02-18
*   NBMiner v27.0 (added support for HNS & HNS_ETH mining for Nvidia GPUs, minor bug fix and improvements)
*   CPUminer-opt-jayddee v3.12.3.1 (bug fix)
*   CPUminer-opt-rplant v4.5.4 (new codebase, optimized lyra2*, optimized minotaur AES/SSE4.2, improved yescryptr8g and lyra2z330 if HT enabled)

##### 0.6-119@200217 2020-02-17
*   Misc minor fixes
*   SRBminer-Multi v0.3.4 (fixed share accepted/rejected display issue with 6block pool, fixed miner auto restarting issue, tiny hashrate increase on 'bl2bsha3' with some GPU's)
*   Bminer v16.0.6 (improved the performance of Cuckaroo29m, fix the regression that the Cuckatoo / Cuckoo miners failed to start)

##### 0.6-118@200216 2020-02-16
*   XMRig (unified) v5.6.0 (fixed generic OpenCL code for AMD Navi GPUs, added health information for AMD GPUs, fixed possible nicehash nonce overflow in some conditions)

##### 0.6-118@200215 2020-02-15
*   Improved optional package `repo-mirror` (now checks for already running instance)
*   Improved miner start/stop procedure
*   Yet another fix for logs rotation
*   Minor fixes in Wi-Fi installation
*   Minor `net-test` fix
*   SRBminer-Multi v0.3.3 (added bl2bsha3 algorithm, RandomX fixes and optimizations)
*   NanoMiner v1.8.1 (fixed issue with incorrect Ethash pool protocol auto-detection on some connections, removed pool.pascalpool.org from list of default Pascal pools)
*   RHminer v2.2b (improved pool connection, code cleanup and minor improvements, removed pool.pascalpool.org)
*   CryptoDredge v0.23.0 (new algos: mtp-tcr, cn-ipx2, cn-zls; improved mtp, cn-gpu; bug fixes)
*   CPUminer-opt-jayddee v3.12.3 (faster avx2 & avx512 for skein, skein2, fixed avx2 for skunk, xevan, skein, skein2)
*   CPUminer-opt-rplant v4.0.31 (added algos: minotaur, lyra2tdc)

##### 0.6-117@200208-2 2020-02-08
*   Bminer v16.0.5 (improved performance C29m)

##### 0.6-117@200208 2020-02-08
*   Fixed `nvidia-oc` (now restores default values for empty OC parameters)
*   Fixed X server start on some configuration with Nvidia cards
*   Minor fix for `motd`
*   SRBMiner-Multi v0.3.1 (CPU & AMD GPU miner which supports m7mv2, defyx, yespower & randomx and their variants algos on CPU, blake2b, blake2s, mtp and some other algos on GPU)
*   NanoMiner v1.8.0 (added Cortex support for AMD Radeon RX 570 16G cards, improved RandomHash2 performance up to +30% for some of CPUs)
*   Bminer v16.0.4 (improve the performance of C29m miner, reduce the rejection rate of the C29m miner)
*   RHminer v2.2 (performance improved up to 55% depend on CPU type)
*   CPUminer-opt v.3.12.1 (faster implementation phi2 on avx2 and avx512 capable CPU, improved log output, bug fixes)

##### 0.6-116@200203 2020-02-03
*   RHminer v2.1c (fixed a lot of bugs, improved hashrate up to 2%)
*   lolMiner: fixed stat on some algos

##### 0.6-116@200202 2020-02-02
*   Improved `nvidia-oc`
*   Improved `motd` (show help only on session start; show miner fork name)
*   Updated `amdmeminfo` (added ID for RX 5500 XT and RX 5600 XT)
*   RHminer v2.1b (small fix vs v2.1)
*   XMRig v5.5.3 (optimization and fixes)
*   TT-Miner v3.2.3 beta-1 (experimental release)
*   Bminer v16.0.3 (improved performance and stability of the C29m)
*   CPUminer-opt v3.11.8 by JayDDee (fixes and optimization)
*   lolMiner: added missed mode `GRIN-AUTO` (Grin Auto Profit Switcher: works on some pools, see miner's manual)

##### 0.6-115@200130 2020-01-30
*   Improved `net-test` (added CA1 mirror, compact output to fit more into screen)
*   Improved miners log rotation (fixed logs truncation bug, increased truncate log size to 20MB, rotate logs before truncation, keep up to 10 logs per miner, gzip logs to save space)
*   Improved `agent` (prevent  from starting too early in some cases and breaking OC)
*   Improved `motd` (show miners version in flightsheet info)
*   Improved `nvidia-info` (added gpu temp, fans rpm, uuid and link width)
*   CPUminer-opt by JayDDee v3.11.7 (added yescryptr8g and sha3d algos)
*   miniZ v1.5t (hashrate improvements for 150,5 and 210,9: up to 4% and up to 2% on other depending on algo and GPU, better support for GTX 1660 Ti, improved stability)
*   lolMiner v0.9.7 (increased GRIN-C32 performance on Vega, VII & Navi cards by 15-18%)

##### 0.6-114@200125 2020-01-25
*   Enabled mining in maintenance mode
*   CPUminer-opt by JayDDee v3.11.6 (fixed CPU temperature regression, improved log output)
*   Bminer v16.0.2 (performance improvement on Cuckaroo29m)
*   NanoMiner v1.7.3 (significant up to x5 performance improvements for RandomHash2 algo)
*   RHminer v2.1 (significant increase hashrate, fixed bug with exiting from main thread)

##### 0.6-113@200122 2020-01-22
*   XMRig-BigBangСore v1.2 (XMRig for cpu 3.1.3 based code; improved POW hash algorithm of CryptoNight)
*   TeamRedMiner: small update for sync changes with Miner configuration dialogue

##### 0.6-113@200121 2020-01-21
*   Fixed potential bug in `hive-replace`
*   Improved restart hanged `agent`
*   Gminer v1.96 (improved cuckaroom29 performance up to +5-6% dependent on GPU)
*   CPUminer-opt v3.11.5 (fixes and improvements)
NanoMiner v1.7.1 (added Ethash support for AMD Navi 12 and Navi 14 GPUs including AMD RX 5500)
*   lolMiner v0.9.6 (significant improvement on GRIN-C29M performance: +6-7% on 580 and Vega cards, +10% on Navi, significant improvement on GRIN-C31 and GRIN-C32 solver: ~ +6% on all AMD cards, added a 16G GRIN-C32 solver: approx 20% faster on Radeon VII, Vega FE and 570 16G)
*   Bminer v16.0.1 (fix the Cuckaroo29m miner fails to start on Turing-based cards or cards that have only 4G memory, fix the Cuckaroo29m miner submits shares that have low difficulty, performance improvement on the Cuckaroo29m)
*   RHminer v2.0 (added support RandomHash2 algo)

##### 0.6-112@200116 2020-01-16
*   Updated `amd-info` tool (display of card names on motherboards using PCI-E hubs is fixed)
*   Fixed `amd-oc` and `gpu-stats` to use on rigs with modern AMD iGPU
*   Fixed `nvidia-oc` for Nvidia GTX 1660 Super
*   Bminer v16.0.0 (initial support for the Cuckaroo29m algorithm)

##### 0.6-111@200115 2020-01-15
*   Fixes and improvements for `motd` (added GPU drivers versions and flightsheet info, improved watch mode)
*   Small fix Wi-Fi drivers installation script
*   NanoMiner v1.7.0 (fixed issue with Floating point exception at startup observer on some CPUs)
*   Gminer v1.93 (added Cuckaroom29 with 3% devfee, added Cuckarood29v with 10% devfee, fixed "No shares" bug for Eaglesong when extranonce length not equal to 4)
*   lolMiner v0.9.5.1 (added support for Grin-C29M, improved C31 performance on 8G cards by ~5%, slightly lowered energy use of C31/C32 solver)
*   TeamRedMiner: fixed sending worker name for Ethash pools

##### 0.6-110@200112 2020-01-12
*   Slightly improved `hugepages` tool (change Intel CPU's MSR boost from 6 to 15)
*   Added `cpu-temp` tool (get CPU temp)
*   XMRig (unified) v5.5.1 (default value for Intel MSR preset changed to 15, fixed unwanted resume after RandomX dataset change)
*   Z-Enemy v2.4 as ccminer fork (fixed high CPU load with latest nVidia drivers)

##### 0.6-109@200110 2020-01-10
*   Slightly changes in`miner` (added comment on log truncate)
*   Reworked GrinGoldMiner to use forks
*   MoneroVMiner v1.1 (fix CUDA, GrinGoldMiner fork)
*   XMRigCC v2.5.0 (sync with mainline XMRig sources)
*   XLARig v5.0.1 fork of XMRig (unified) (rebase to XMRig v5.4.0, defyx optimization and fixes)
*   CPUminer-opt by JayDDee v3.11.2 (optimization and fixes)
*   PhoenixMiner v4.9c (added support for AMD RX5500, added support for AMD Linux drivers 19.50-967956, fixed the problem with loading NVML with the latest Nvidia drivers)

##### 0.6-108@191231 2019-12-31
*   Minor fix for `disk-expand` tool (expand filesystem if it is smaller than partition)
*   NEW MoneroVMiner v1.0 (special version of GrinGoldMiner for MoneroV coin)
*   XMR-Stak-RX v1.0.4 (NUMA support/better autoconfig, implemented Ryzen speedups)
*   XMRig (unified) v5.5.0 (removed rx/v, added cryptonight-talleo, fixed crash on very low memory systems, added fix for Ryzen 1st-gen crashes, added support for environment variables in config file)
*   CPUminer-opt v3.10.7 by JayDDee (added AVX512 for x25x, lbry, x13bcd (bcd))
*   Gminer v1.92 (fixed miner id for BBC which allowed mining on bbcpool.io pool)

##### 0.6-107@191227 2019-12-27
*   Fixed update error (that occurred when updating to v0.6-106 on some installations)

##### 0.6-106@191226 2019-12-26
*   Improved `motd` with new feature `motd watch` (console live stats and logs on rigs, added swap file info if enabled)
*   Rebuild `hssh` with static libs for better compatibility
*   Gminer v1.91 (added support mining BBC coin, added solo mode for KDA/Kadena with option `--proto solo`)
*   CPUminer-opt-rplant v4.0.29 (added yespowerITC for ITC/Intercoin)
*   CPUminer-opt-JayDDee v3.10.6 (added support for SSL stratum, added AVX512 support x21s, x22i, lyra2z, allium, x17, sonoa, xevan, hmq1725, lyra2rev3, lyra2rev2, faster hmq1725 AVX2 implementation)

##### 0.6-105@191221 2019-12-21
*   Improved `swap-file` (ultra fast swap file creation, set default size to 4GB, removed total memory option)
*   NEW nheqminer-verushash v0.8.0 (fork for CPU mining VerusHash 2.1)
*   XMRig (unified) v5.4.0 (added RandomSFX and RandomV, added reverting MSR changes on miner exit, fixed crash on first generation Zen CPUs)

##### 0.6-104@191219 2019-12-19
*   Improved `hugepages` (better error handling, new options `-mc1`, `-mc2`, `-mc3`)
*   Minor fixes for `wd`
*   XMRig (unified) RandomSFX v5.4.0 (Safex-Rig v1.2)
*   XMRigCC v2.2.2 (added CPU max threads option `cpu-max-threads-hint`, fixed autoconfig/autosave for rx/loki)
*   XMRig (cpu): added HugePages autotune feature
*   Gminer: fixed dual mode ethash+blake2s (eth+kda)

##### 0.6-103@191218 2019-12-18
*   Improved `hugepages` tool (added RX boost for AMD Ryzen family, added new mode `-erx` use 1Gb HugePages for RandomX if it's possible and if not then the action is similar to the `-rx` option, better error handling)
*   Improved `agent` (added restart hanged gpu-stats, added reporting available RAM instead of just free memory, reboot if filesystem is mounted read-only)
*   Improved `firstrun` (added more strict checking of api host url input)
*   Improved `selfupgrade` and miners installation (check available memory and stop miners in advance)
*   Added installer for optional WiFi drivers (/hive/opt/wifi/wifi-installer.sh)
*   Reworked software watchdog  `wd` (code refactoring)
*   Fixed OC for GTX 1660 (without Ti)
*   NEW CCminer-verus v3.611 (VerusHash 2.1 CUDA miner; Notes: need CPU with AES and AVX support)
*   NEW XMRig-BigBangCore v3.1.3 (based on code of XMRig (cpu) for cn/bbc algo - BBC/BigBangCore coin)
*   NEW XMRig-RandomV v5.3.0 (based on code of unified XMRig for RandomV algo - XMV/MoneroV coin)
*   NEW XMRig-RandomSFX v5.0.2 (based on code of unified XMRig for RandomSFX algo - SFX/Safex Cash coin)
*   TT-Miner v3.2.2 release (improved Blake2S performance)
*   CPUminer-opt v3.10.4 (added AVX512 for X* family algos)
*   XMRig (unified) v5.3.0 (v5.2.1: added support for AMD Ryzen MSR registers - up to +6% hashrate improvement ; v5.3.0: increased stratum send buffer size)
*   XMR-Stak-RandomX v1.0.3 (added 1GiB page support, added ArQma support, optimize hash calculation)
*   lolMiner v0.9.4 (new GRIN-AT31 performance code for Vega up to +7% and Navi up to +12%, added experimental support for cuckatoo-32)
*   Gminer v1.88 (v1.86: added blake2s algorithm for Nvidia, added ethash+blake2s dual solver, decreased stale shares percentage on pool side for C31; v1.87: added blake2s support for AMD, v1.88: fixed performance regression for Cuckatoo31 algorithm on P104-100)

##### 0.6-102@191212 2019-12-12
*   Gminer v1.85 beta (added blake2s algo for KDA/Kadena mining, decreased stale shares percentage on pool side for cuckatoo31 algorithm)
*   XMRigCC v2.2.1 as fork XMRig (integrated RandomSFX algo: rx/sfx, performance improvements for RandomX variants)

##### 0.6-102@191211 2019-12-11
*   Improved `hive-replace` tool (more info added for interactive mode, added option `--repo=URL` for list and install images from custom location http/ftp)
*   lolMiner v0.9.3 (extended GRIN-AT31 compatibility to older drivers 18.xx, deeply reworked kernel scheduler, fixed GRIN-AT31 kernel bugs: improving stability and fidelity)
*   CPUminer-opt JayDDee v3.10.2 (AVX512 added for bmw512, c11, phi1612 (phi), qubit, skunk, x11, x11gost, fixed c11 AVX2 invalid shares)
*   TT-Miner v3.2.1 latest (fixed KDA/Kadena solo - no new work, slightly improved hashrate for Blake2S for NVidia GTX 10xx cards)
*   TT-Miner v3.2.2 beta-2 (performance improvements for Blake2S, add new option for KDA/Kadena solo: `-sbc`: select best Kadena ChainID, fixed ethash algo was not available for CUDA 10.1)
*   XMRig (unified) v5.2.0 (improved hashrate by 1-2% by adding 1GB huge pages support with new option `1gb-pages` in `randomx` object - need at least 3G free RAM, added automatic huge pages configuration, added automatic Intel prefetchers configuration with new option `wrmsr` in `randomx` object, new performance optimizations for Ryzen CPUs)

##### 0.6-101@191209 2019-12-09
*   NoncerPro Kadena Miner v2.0.2 (fixed a critical kernel issue of v2.0.1 on non RTX nvidia cards)

##### 0.6-101@191208 2019-12-08
*   Fixed `wifi` command (for Ubuntu 16.04 based images)
*   Small fixes for `motd` command (fixed padding on some configurations, added more hints to commands FAQ, revert back gpu indexes sequence for mixed rigs)
*   TT-Miner v3.2.0 (release)
*   NoncerPro Kadena Miner v2.0.1 (added support for pool mining: option `--pool` for pool mining and `--solo` for solo mining, hashrate improvement for some AMD/Nvidia cards, reduced devfee to 2%)

##### 0.6-100@191207 2019-12-07
*   Improved `nvidia-oc` tool (now shows error when GPU were not properly detected)
*   Improved `hugepages` tool (implemented Intel CPU's RandomX booster - up to +30% more hashrate power on newer Intel CPU's, improved autotune on multi CPUs system)
*   Improved `hive-replace` (added new options for easy management)
*   Improvements and fixes for `wifi` command (added wifi network scanning and selection from list, fixed special symbols handling in ssid and password)
*   Improved `firstrun` command (added offer to setup wifi if no active connection and and question to try again on fail)
*   Improved `sreboot` command
*   Improved `motd` command (new nice boot screen for rig)
*   Improved `helpme` command (updated commands list)
*   Updated hints output for several command including `miner`
*   Gminer v1.83 (improved Eaglesong performance on Nvidia GPUs)
*   XMRig (unified) v5.1.1 (fixed various system response/stability issues, added new CPU option yield, fixed wrong priority of main miner thread)
*   TT-Miner v3.2.0 beta7 (small performance improvements for mining KDA/Kadena, added new options: `-tbr`, `-cid`)
*   CPUminer-opt v3.10.1 (added AVX512 for blake2b, nist5, quark, tribus)
*   CPUminer-opt by rplant v4.0.28 (added support yespowerIOTS, yespowerIC, sha256csm)
*   Spark miner: fixed stats (fixed bug when shares cards with another miner)
*   XMRig (unified): fix temp in stats for AMD processors
*   XMRig (unified), XMR-Stak: implemented RandomX autotune if HugePages not set

##### 0.6-99@191204 2019-12-04
*   Improved `autofan`  (restart autofan on errors, resume mining after overheat when reaching target temp)
*   XMR-Stak v2.10.8 (AMD: optimize auto adjustment, optimize unroll for rx5700, remove monero support, fixed other issues)
*   lolMiner 0.9.2 significant performance improvement of GRIN-AT31 on 8/16G cards up to +5% on Polaris & Vega and up to +10 on Navi)
*   TT-Miner v3.2.0 beta5 (add support for mining KDA/Kadena, added support SSL)
*   CPUminer-Opt by JayDDee v3.10.0 (added support AVX512 on argon2d, blake2s, keccak, keccakc, skein & skein2, fixed some issues)

##### 0.6-98@191201 2019-12-01
*   XMRig (unified) v5.1.0 (improved RandomX performance: up to +6-7% on Intel CPUs and +2-3% on Ryzen CPUs)
*   XMR-Stak-RandomX v1.0.2 (optimize and slightly bit improved hashrate)

##### 0.6-98@191130 2019-11-30
*   Added new tool `hugepages` for tuning HugePages (XMR-Stak and XMRig (unified) can be tuned from web interface - new field added to miner settings)
*   Gminer v1.82 (significant performance improvements for cuckoo29 algorithm (AE, BFC) on Nvidia GPUs up to +10%)
*   lolMiner 0.9.2 beta (improved performance on GRIN-AT31 for 8 and 16G cards by 2-8%. Please note: 4G solver for GRIN-AT31 disabled, due beta status choose version in miner settings)
*   TeamRedMiner v0.6.1 (added pool failover and load balancing, added better error messages when failing to allocate eth DAG buffers, added automatic setting for environment variables for 4GB GPUs, added report of pool stats and fixes for submitting hashrate to pools, changed initial pool auto detect mode to eth proxy)
*   XMR-Stak: fixed stats for 12+ GPU rigs
*   Fixed CPU threads output: CKB-miner, FinMiner/NanoMiner
*   NoncerPro Kadena Miner: fixed config generation if user extra config not empty

##### 0.6-97@191128 2019-11-28
*   Improved support for some third-party hardware
*   NEW NoncerPro Kadena v1.3.1 (OpenCL / CUDA GPU miner for KDA/Kadena, will be added to interface later today)
*   Gminer v1.80 release (the same as beta + support more Ethash coins: PIRL, CLO, ETP, EXP)
*   Gminer v1.81 (fixed bug with invalid worker name for cortex)
*   CPUminer-Opt by JayDDee v3.9.11 (added x22i, x25x algos support)
*   XMR-Stak-RandomX v1.0.1 (bug fixes)

##### 0.6-96@191126 2019-11-26
*   Gminer v1.80 Beta (added support mining CTXC/Cortex coin: requires 8G+ cards, devfee 5%, choose version in miner settings)

##### LINUX IMAGE RELEASE 0.6-96 2019-11-25
*   Hive Linux client image: 0.6-96@191125 (new stable branch based on Ubuntu 18.04)
*   Universal boot mode: BIOS | UEFI
*   Linux kernel: 5.0.21
*   Drivers version: AMD v19.20, Nvidia: v440.31

##### 0.6-96@191125 2019-11-25
*   Improved `selfupgrade` command and miners installation procedure
*   Fixed `hello` command for some system configuration
*   Fixed compatibility some third-party hardware with Chinese watchdogs
*   Added new commands for watchdog-opendev (use `watchdog-opendev` without args to get help)
*   Better output for `helpme`, `amd-oc` commands
*   PhoenixMiner v4.8c (the same as in 4.8b + added command-line option `-gbase` to set 0-base or 1-based GPU indexes, default is 1)
*   lolMiner v0.9.1 (added GRIN-AT31 solver for 16G AMD cards, updated GRIN-AT31 solver for 4G AMD cards, fixed a bug causing too low pool hash on GRIN-AT31, added experimental GRIN-AT31 support for AMD Navi)
*   CPUminer-Opt by JayDDee v3.9.10 (faster X* algos CPUs with AVX2, small improvements to summary stats report)
*   XMR-Stak:  fixed stats for legacy AMD CPUs

##### 0.6-95@191123 2019-11-23
*   TeamRedMiner v0.6.0 (added ethash support)
*   Gminer v1.79 (fixed bug with ETH+CKB solver)
*   TT-Miner v3.1.1 (fix a bug in dual mine EPIC & other coin)

##### 0.6-94@191121 2019-11-21
*   Improved `net-test` (runs traceroute to API server if it is unreachable)
*   NBMiner v26.2 (improve CKB+ETH performance on AMD GPUs, fixed bug v26.1 when miner crashed on launch on certain AMD rigs)
*   Gminer v1.78 (added option to control ETH/CKB balance in dual mining, fixed bug with x2 hashare in miner output on eaglesong algo)
*   TT-Miner v3.1.0 (added support for CUDA 10.2, added eaglesong, removed myr-gr, teohashv1, bug fixes)
*   Fixed stats for Spark Miner

##### ASIC 0.1-13 2019-11-21
*   Added support of Antminer S9k, S9SE, T15,S15, T17, S17, S17pro
*   Added support of Innosilicon T2*, T3*
*   Added support Hiveon ASIC S9 firmware v1.02
*   Other minor fixes and improvemnts

##### 0.6-93@191120 2019-11-20
*   Gminer v1.77 (decreased stale shares on pool side for C31 algo)
*   Spark Miner v0.4.1 (improved parallel work with Сlaymore's ETH miner)

##### 0.6-92@191119 2019-11-19
*   Updated `amdmeminfo` tool (added some IDs of RX 5700 series)
*   Improved `net-test` (now shows current API connection not only server)
*   Updated `amd-oc` (introducing  further support of OC/UV Navi cards)
*   Fixed `agent` (switch push interval back to default)
*   XMRig (unified) v5.0.1 (fixed compatibility with some AMD GPUs)
*   lolMiner v0.9 (significant performance improvement for C31 on 8G AMD cards, reduced stale GRIN shares, bug fixes)
*   Gminer v1.76 (improved ETH+CKB performance, reduced stale shares on C31)
*   nq-miner v0.99.6 (fixed automatic memory allocation bug, fixed json API)

##### 0.6-91@191118 2019-11-18
*   TT-Miner v3.1.0 Beta3 (add support for EagleSong, removed support of Myr-Gr and TeoHashV1 algo)
*   Fixed installation XMR-Stak-RandomX package

##### 0.6-90@191117 2019-11-17
*   Fixed config generator for PhoenixMiner (it was affect only to users with extra config settings)
*   Fixed potential math bug with very big hashrate values (Bminer, NBMiner)

##### 0.6-90@191116 2019-11-16
*   Improved `net-test` tool (now shows resolved ip, current api server and more local network info, added output advanced info using option `-a|--advanced`)
*   Improved `watchdog-opendev` (added sleep time check to stop pinging wd on very high LA)
*   Improved `autofan` (small algo improvement, added commands `start|stop|restart|log`)
*   NEW nq-miner v0.99.5 (Nimiq GPU miner for AMD and Nvidia GPUs)
*   NEW XMR-Stak-RandomX v1.0.0 (free all-in-one CPU/OCL/CUDA RandomX miner which supported only randomx and variants (loki,wow)
*   NEW XMRig (unified) v5.0.0 (XMRig now unified CPU/OCL/CUDA miner for Argon2/RandomX/Cryptonight based algos)
*   NBMiner v26.1 (add support for mining CKB+ETH on AMD GPU, improved performance for mining CKB on Nvidia GPUs
*   Gminer v1.75 (reduced memory usage for Cuckatoo31 8GB solver, added Ethash+Eaglesong dual mining for Nvidia GPUs)
*   Miner config/stats fixes and improvements (PhoenixMiner, Gminer, XMR-Stak)
*   Other small fixes and improvements

##### 0.6-89@191115 2019-11-15
*   CKB-miner v0.25 (CKB node miner ready to mainnet)
*   Gminer v1.74 (significant performance improvements for сuckatoo31 algo)

##### 0.6-89@191114 2019-11-14
*   Issue fix: minor `autofan` fix
*   Spark Miner v0.4.0 (renamed from s-mine; CKB mainnet ready miner for AMD cards; can be launched simultaneously with claymore's or other ethereum miner, use `-scale X` option where X scale factor in range 10-30, 0 for auto, 14-17 for eth dual mining)
*   miniZ v1.5s (improvement for 125/4, 150/5/3 and 144/5 algos from 0.3% to 3% depending on algo and GPU)

##### 0.6-88@191113 2019-11-13
*   Issue fix: `autofan` bug (on some configurations, there may be jumps in fan speed over a short period of time)

##### 0.6-87@191112 2019-11-12
*   Issue fix: `amd-info` minor fix 
*   Issue fix: `nvidia-oc` minor fix
*   Improvement: `agent` fixes and improvements (improved json building and checking to solve issues with bad requests  to Hive API servers; replaced password with asterisks in `hello` and `agent-screen` output; `agent` now restarts itself in screen on crash; added new commands - `agent-screen [start|restart|stop|log|log1|log2]`)
*   Improvement: `autofan` improvement
*   Improvement: update k10temp module (added some CPU support)
*   Gminer v1.73 (re-added eaglesong(CKB) algo for Nvidia/AMD)
*   PhoenixMiner v4.8b (added support for the latest AMD drivers under Linux 19.30-934563)
*   SGminer-fancyIX v5.6.1.3.b6a "0.6.0-1 release" (improved mtp performance - syncup with zcoinofficial repo)
*   NanoMiner v1.6.2 (fixed setting up RandomX algo)
*   EggMinerGPU fix: stats fixed for EggMinerGPU v4.0.200

##### 0.6-86@191107 2019-11-07
*   Issue fix: miner start exit code fixed
*   Issue fix: `nvidia-oc` was not applied with large delay values (delay now limited to 150sec and also prevent simultaneous `nvidia-oc` runs by killing already running)
*   Improvement: increased width of top processes for output triggered by watchdog event "High LA"
*   Improvement: minor improvement in multiple miners start
*   Gminer v1.72 (added ethash algo support for ETH/ETC coins, also supported NiceHash/MiningPoolHub pools with `--proto stratum` option)
*   CKB-miner v0.24.0 (updated to CKB v0.24)
*   CCminer-djm34 v1.3.1 (corrects a memory leak which may cause ccminer after a long while if the ressources ram/virtual memory are limited)
*   WildRig-Multi v0.20.1 (up to 5% hashrate speedup for mtp/mtp-tcr on Navi, fixed x22i incorrect shares)
*   TT-Miner v3.1.0 Beta2 (improvements for MTP - mostly for RTX cards)
*   lolMiner stats issue workaround: in some algos lolMiner API not incremented submitted shares but counting accepted shares which breaks ASR
*   CPUminer-opt and XMRig fix: temperature readings fixed (mostly for AMD Ryzen)
*   Ethminer fix: fallback to v0.17.1 as "Latest" due buggy API in v0.18.0 (if you like v0.18.0 you can choose it in miner settings)

##### 0.6-85@191028 2019-10-28
*   `cache-hive-ip` fixes and improvements
*   Issue fix: report all connected disks to web, not only system
*   Issue fix: `nvidia-oc` now reports error if setting power limit fails
*   Issue fix: `autofan` unable set fan speed to MAX in some situations
*   Improvement: added info to `autofan` "unable to set fan speed" message
*   Improvement: `miner log` now reports if session is active or not
*   Improvement: added `miner status` command to get running screen sessions without opening them
*   Improvement: watchdog now sends miner logs with low hashrate message and top processes list on high LA
*   Improvement: improved API sockets close on miner start
*   CCminer-djm34 v1.3.0 (fix a bug in solo mining)
*   XMRigCC v2.1.0 (as XMRig fork - full rebase on XMRig v3.2.0)
*   WildRig-Multi v0.20.0.3 (added support of mtp and mtp-tcr algo, added new arguments `--opencl-less-cpu-load` and `--split-job`)
*   TT-Miner v3.1.0 Beta1 (small improvements for all ProgPoW variants)

##### LINUX IMAGE RELEASE 0.6-84 2019-10-21
*   Hive Linux client image: 0.6-84@191021 (new stable branch based on Ubuntu 18.04)
*   Universal boot mode: BIOS | UEFI
*   Linux kernel: 5.0.21
*   Drivers version: AMD v19.20, Nvidia: v430.50

##### 0.6-84@191021 2019-10-21
*   Improved Autofan (improved algorithm, improved compatibility with custom mining cases)
*   Issue fix: soft-WD now also stops when `miner stop` command applied
*   CKB-miner v0.23.0 (updated for CKB v0.23)
*   miniZ v1.5r (performance improvement for EQ 210/9 up to 7%, improved stability)

##### 0.6-83@191017 2019-10-17
*   Autofan small fix (force set min_fan=25% for AMD GPU)
*   Added output for some additional temps in `amd-info` if they exist
*   Gminer v1.70 (fixed bug in BFC stratum leading to "low difficulty" shares after changing target)
*   NanoMiner v1.6.1 (more Ethash memory optimizations for Nvidia cards, SSL connections for Nanopool ETH, ETC pools are used by default if no pools provided, Ubiqpool.io pools are used by default if no UBQ pools provided)
*   NEW CCminer-tecracoin v1.2.4 (based on djm34 code added custom mtp implementation mtp-tcr for Nvidia)
*   NEW SGminer-tecracoin v0.1.4 (based on djm34 code added custom mtp implementation mtp-tcr for AMD)
*   NEW CPUminer-opt fork RKZ by RicKillerZ v4.2b (optimized for yespower variants CPUminer-opt version)

##### 0.6-82@191016 2019-10-16
*   Improved Autofan
*   Gminer v1.69 (added BFC mining on Nvidia and AMD cards)
*   T-Rex v0.14.6 (bug fixes)
*   WildRig-Multi v0.19.3 (fixed x16rv2 algo)
*   NEW CPUminer-opt fork by rplant v4.0.20 (supported some CPU coins on yespower based algos)

##### 0.6-81@191011 2019-10-11
*   small fix which affect only for PXE image
*   TT-Miner v3.0.10 Release (all changes in 3.0.10 beta + fixed an bug that interrupts the API connection under some conditions, added a watchdog for EPIC connection)
*   PhoenixMiner v4.7c (since the 4.7b beta small improvements)
*   Gminer v1.68 Beta (removed eaglesong algorithm support, improved performance for Cuckarood29/Cuckaroo29s/Aeternity algos)
*   NBMiner v26.0 (added support for BFC mininig on Nvidia, fixed CKB compatibility on AMD, fixed cuckoocycle on nicehash)
*   WildRig-Multi v0.19.2 (added support x16rv2 algo)
*   CPUminer-opt v3.9.9 (added power2b algo, added generic yespower-b2b)

##### 0.6-80@191008-2 2019-10-08
* fixed selfupgrade problem with release 0.6-79@191008

##### 0.6-79@191008 2019-10-08
*   fixed droptcpsock-dkms dependency which occurred in some cases
*   TT-Miner v3.0.10 Beta4 (bug fixes)
*   CCminer-djm34 v1.2.3 (stability improvement)

##### 0.6-78@191007 2019-10-07
*   TT-Miner v3.0.10 Beta3 (improved performance for ProgPoW based algos, auto detection of the max supported compute capability)
*   CCminer fork Z-Enemy v2.3 (performance improvement: +2-3% x16rv2 algo)
*   T-Rex v0.14.5 (small fixes)

##### 0.6-78@191006 2019-10-06
*   PhoenixMiner v4.7b (reduced VRAM usage for both AMD and Nvidia cards, added support for mining QuarkChain [QKC] without DAG switching on devfee use `-coin qkc`)
*   Bminer v15.8.7 (improved the performance of Beam for RTX cards, experimental support for dual-mining Ethash and Eaglesong algorithm)

##### 0.6-78@191005-2 2019-10-05
*   S-Mine v0.3.1 (reduced chance for stale shares)
*   CKB-miner v0.22.0.1 (updated for CKB v0.22)
*   NBMiner: fixed Ethash stats in CKB+ETH mode

##### 0.6-78@191005 2019-10-05
*   `opendev-watchdog` minor fixes
*   S-Mine v0.3.0 (updated CKB statum protocol, improved performance, bug fixes)
*   NBMiner v25.5 (improved CKB mining performance on both NVIDIA & AMD cards, improved CKB+ETH performance on NVIDIA cards, added support for mining SERO on AMD cards, added a new option `--platform` to allow users to choose GPU platform)

##### 0.6-77@191002-2 2019-10-02
*   CryptoDredge v0.22.0 (added x16rv2 algo, fixed ccminer API, fixed stratum issue related to 'resource deadlock would occur', other minor fixes. Available versions builded with CUDA 9.2/10.0(default)/10.1 toolkits)

##### 0.6-77@191002 2019-10-02
*   Reworked miner restart procedure to minimize delays while restarting
*   `gpu-fans-find` fixes for AMD rigs, added fans stop checking
*   CPUminer-opt by JayDDee v3.9.8.1 (small changes in generation of summary log report)
*   NanoMiner v1.6.0 (added support RandomHash2 and RandomX algos; Cuckarood29 performance improved up to 24% on AMD and Nvidia)

##### 0.6-76@190928 2019-09-28
*   Gminer v1.67 (performance improvements for `cuckarood29` specially on RTX cards)
*   XMRig v3.2.0 (added per pool option `coin` with single possible value `monero` for pools without algorithm negotiation)

##### 0.6-76@190927 2019-09-27
*   TT-Miner v3.0.9 Beta1 (added information about the DAG size and the available memory, another bugfix with the device option: `-d`, removed library depency to CUDA 10.1 for ProgPoWZ and Ubiq)
*   Added support CPUminer-opt forks
*   CPUminer-opt v3.9.8 (added x16rv2, changes to log output to provide data more relevant)
*   NEW CPUminer-opt-cpupower v3.9.5.2 (fork `cpupower` of CPUminer-opt for CPUchain coin)

##### 0.6-75@190926 2019-09-26
*   reworked miner start/stop procedure
*   improved `nvidia-driver-update` tool
*   slighty improved `disk-expand` tool
*   TeamRedMiner v0.5.9 (added x16rv2 algo; optimization work on x16r: +8-10% hashrate, mem clock no longer as important; issue fix: kernels split into multiple binaries to fix linux amdgpu-pro driver issues)
*   TT-Miner v3.0.8 (added support ETHASH coins MUSIC, EXP; fixed the device selection option: `-d`)

##### 0.6-74@190925 2019-09-25
*   CKB-miner v0.21.1 (fixed OpenCL bug)
*   T-Rex v0.14.4 (added ability to auto-switch mining algorithm using new `--fork-at` parameter)
*   TT-Miner v3.0.6 Release (faster start, bug fixes known for v3.0.6 Beta series)
*   Z-Enemy v2.2 (added x16rv2 algo, added support for secure stratum+ssl connections. Note: miner is in CCminer settings as fork `enemy`)
*   GMiner v1.66 (significant performance improvements for cuckarood29 up to +10%)

##### 0.6-73@190922 2019-09-22
*   Added new features and options to `nvidia-driver-update` tool. Bug fixes
*   Added call `disk-expand` on newly installed rig
*   Issue fixed: `selfupgrade` now stops miners, watchdog, autofan during update
*   TT-Miner v3.0.6 Beta4 (aadded ability switch to alternate mining algo when ProgPoW idle on Epic)
*   TeamRedMiner v0.5.8 (added chukwa algo support, issue fixed: kernels not loaded properly for Conceal, added logic for pool reconnect on N rejected shares in a row)
*   XMRig v3.1.3 (fixed possible duplicated shares after algorithm switching)
*   CKB-miner v0.21.0 (update to CKB v0.21.0)
*   NEW XLArig v3.2.0 (XMRig fork for defyx algo for mining XLA Scala - ex Stellite coin)
*   NEW SparrowMiner-UPX2 v2.1.2 (XMR-Stak fork for support cryptonight-upx2 algo and can be found as fork called `uplexa`)

##### 0.6-72@190918 2019-09-18
*   T-Rex v0.14.2 BETA (fixed x16rv2 issue where the pool hashrate was lower than reported by the console. Note: select version in miner settings)

##### 0.6-72@190917 2019-09-17
*   T-Rex v0.14.1 BETA (added x16rv2 algo. Note: select version in miner settings)
*   Gminer v1.65 (support eaglesong mining on AMD cards)
*   XMRig v3.1.2 (many RandomX optimizations and fixes)

##### 0.6-71@190915-2 2019-09-15
*   fixed broken AMD fan control
*   fixed cortex-miner package

##### 0.6-70@190915 2019-09-15
*   fixed manual fan control for AMD
*   Gminer v1.64 (added support for CKB mining: eaglesong algo)
*   CCminer-djm34 v1.2.2 (improved solo mining)
*   PhoenixMiner v4.6c (since the v4.6b added ability to show the current hotspot (junction) and memory temperatures on AMD cards when `-hstats 2` option is used)
*   miniZ v1.5q6 (performance improvement for 192/7, added `--jobtimeout`, `--retries`, `--retrydelay` for (re)connection customization)
*   TT-Miner v3.0.6 Beta1 (add support mining EPIC at ProgPoW algo: use `-COIN EPIC` Note: select version in miner settings)
*   **NEW** CCminer-suprminer-spmod v1.6 (supporting x16rv2/x16r/x16s/c11/x17 algos)
*   **NEW** ckb-miner v0.20.0.1 OpenCL
*   **NEW** cortex-miner v1.0.0 (version for Nvidia cards with 11G+ VRAM)

##### 0.6-69@190911 2019-09-11
*   NBMiner v25.2 (added support for CKB mining on AMD card)
*   PhoenixMiner v4.6b (implemented hardware control, added advanced hardware stats with `-hstats 2` option, added support for all new AMD Linux drivers up to the latest 19.30-855429)
*   EggMinerGpu v4.0.200 (upgraded kernel, improved hashrate)
*   Sushi Miner OpenCL v2.1.1 (improved performance)

##### 0.6-69@190908 2019-09-08
*   Added check GPT table on boot
*   Fixed watchdog in maintenance mode
*   Smine v0.2.1 (bug fix)

##### 0.6-68@190907-2 2019-09-07
*   Fixed a bug in `hive-replace` that occurred when it was necessary to recalculate the GPT checksum
*   CKB-miner v0.20.0 (CPU/Nvidia CKB miner)

##### LINUX IMAGE RELEASE 0.6-68 2019-09-07
*   First stable Linux client image from a new branch based on Ubuntu 18.04
*   Universal boot mode: BIOS | UEFI
*   Linux kernel: 5.0.21
*   Drivers version: AMD v19.20, Nvidia: v430.40

##### 0.6-67@190907 2019-09-07
*   Added resending `hello` on connection failures
*   **NEW** CKB-miner v0.19.2 (CPU/Nvidia CKB miner)
*   **NEW** Smine v0.2.0 (AMD CKB miner)

##### 0.6-66@190905 2019-09-05
*   Bminer v15.8.6 (improved the performance of automatic tuning of dual mining parameters)
*   NBMiner v25.0 (added support for CKB mining & CKB+ETH dual mining)

##### 0.6-66@190904-2 2019-09-04
*   XMRigCC v2.0.0 as fork XMRig (based on XMRig v3.1.1 plus support argon2 based algos, cn-upx2, cn-conceal)
*   fixed miniZ v1.5q5 for proper build

##### 0.6-66@190904 2019-09-04
*   Added PCI IDs for new devices to `amdmeminfo`
*   XMRig v3.1.1 (RandomX hashrate improved by 0.5-1.5% depending on variant and CPU, fixed multiple network bugs, other bugs fixes)
*   XMRig-AMD v2.14.6 (fixed multiple network bugs)
*   XMRig-Nvidia v2.14.5 (fixed multiple network bugs, available builds for CUDA 9.2/10.0/10.1)
*   Bminer v15.8.5 (added an API method to stop the miner)
*   Gminer v1.62 (improved performance for ZelCash on RTX cards up to +8%)
*   miniZ v1.5q5 (general performance improvement for 150/5/3, fixed invalid shares on 150/5/3, fixing performance on 150/5/3 for P104, fixing reconnection to pool)

##### 0.6-65@190830 2019-08-30
*   Gminer v1.60 (support AMD cards for ZelCash, improved performance for Equihash 144.5/192.7 on RTX SUPER cards, added OC1 kernel for BeamHashII for GTX 1070)
*   Gminer v1.61 (improved compatibility with large rigs for 13+ GPUs, improved launch time of miner)

##### 0.6-65@190827 2019-08-27
*   Added new optional argument to `selfupgrade` tool - repository address. Use `--help` for view all available options and their syntax.
*   Claymore's ETH v15.0 (supports up to 384 epoch instead 299 on old version, environment variables now sets automatically - required for 4GB AMD cards, added support for Navi cards in ETH-only mode - due driver issues hashrate is very low)
*   Bminer v15.8.4 (improved performance of BeamHashII algo on RTX cards)

##### 0.6-64@190825 2019-08-25
*   miniZ v1.5q2 (hot-fix release for v1.5q)

##### 0.6-64@190824 2019-08-24
*   Fixed OC for GTX 1650
*   miniZ v1.5q (adjusted oc modes for 125/4 and 150/5/3, improved 144/5 on RTX cards, other bug fixes and improvements)
*   TT-Miner v3.0.5 (hot fix for v3.0.4 - added some missed libs)
*   lolMiner v0.8.8 (improved support for BeamHashII for AMD and Nvidia cards)
*   Gminer: fixed issues with AMD cards

##### 0.6-63@190821 2019-08-21
*   Full support of Nvidia RTX cards (OC, fan control, special tools like `gpu-fans-find` and new tool `nvtool`)
*   Optimization of `cache-hive-ip` resolving a number of problems with DNS
*   Gminer v1.59 (minor performance improvements on GTX for Beam, improved perfomance on RTX cards for Beam)
*   TT-Miner v3.0.4 (reduced CPU usage and system-memory requirement for MTP/ProgPoW/ETHASH, several bug fixes)
*   Bminer v15.8.3 (improved the performance of BeamHashII algorithm)

##### 0.6-62@190819 2019-08-19
*   Gminer v1.56 (improved BeamHashII performance on Nvidia cards)
*   TT-Miner v3.0.2 (improved most of the supported algos, fixed miner crash if password-field is too long)
*   XMRig v3.1.0 (added Argon2 algorithm family: argon2/chukwa and argon2/wrkz)

##### 0.6-62@190816 2019-08-16
*   Bminer v15.8.2 (fixed the regression on the BeamHashII fails to start on RTX 2060)
*   NBMiner v24.4 (added support for mining SIPC and fixed SIPC dxpool compatibility, fixed high CPU usage mining SERO with v24.1 & v24.2, fixed Grin intensity)
*   lolMiner v0.8.7 (added support for BeamHashII for R9 AMD cards, fixed an issue with GENX)
*   lolMiner: fixed config generation when failover pools used
*   Gminer: fixed config generation when used failover pools and tls; fixed algo reporting For Beam
*   XMRig: if no "algo" given in miner's config then assume it as "cn/r" (applied to v2.99+)

##### 0.6-62@190815-2 2019-08-15
*   Bminer v15.8.1 (added support the BEAM hard fork - BeamHashII)

##### 0.6-62@190815 2019-08-15
*   added support for NVMe storages
*   miniZ v1.5p (added support for Beam hardfork with autoswitch, improved support EQ 192/7, improved CPU load; drivers version 410+ is required or select the version for CUDA 8.0 in the miner settings)
*   SGminer-djm34 v0.1.3 (improve miner stability in case of bad pool connection)
*   XMRig v3.0.0 (added support for RandomX/XL/WOW, added NUMA support via hwloc, many other improvements and bug fixes)
*   Gminer v1.55 (improved beamhashII auto-switch for pools that doesn't send "fork height" on login)
*   lolMiner v0.8.6 (added support the BEAM hard fork, fixed a bug with the BEAM stratum backend)

##### image release 0.6-61@190813 2019-08-13
*   Special image for AMD VEGA GPUs with built-in support of Radeon VII GPU
*   Image based on Ubuntu 18.04 (other specs: Linux kernel: 5.0.21-hiveos+vega, AMD drivers: amdgpu-pro v19.10)

##### 0.6-61@190810 2019-08-10
*   `selfupgrade` now also accepts `-f` (as well `--force`) to force update and one more fix for "Hive is up to date"
*   VBIOS flashing bug fix: stop autofan & watchdog before AMD VBIOS flash to prevent possible reboots on gpu-stat errors
*   T-Rex v0.13.2 (tensority nonce fix for antpool)
*   CryptoDredge v0.21.0 (added support algos: chukwa, chukwa-wrkz, cn-ccx; added support SSL connections)
*   XMRig v2.99.5-beta (Hive: fixed config generation for v2.99.2-beta and higher, Miner: many bug fixes and improvements)
*   Gminer v1.54 (fixed bug with auto-switching to BeamHashII, added AMD support for BeamHashII, support GRIMM coin for Nvidia and AMD cards)

##### 0.6-60@190806 2019-08-06
*   T-Rex v0.13.1 (bug fixes: [urgent] tensority max nonce for BTM, "Unregistered stratum method" error on some pools)
*   TeamRedMiner v0.5.7 (added support cn-conceal and cuckarood algos)
*   TT-Miner v3.0.1 (bug fix: hashrate reporting; small fixes Hive control scripts)

##### 0.6-60@190805 2019-08-05
*   `net-test` added ping and responce times
*   added more accurate LA checks to watchdog (prevent reboots on short LA peaks)
*   fixed exit code `amd-oc` and `nvidia-oc`
*   `selfupgrade` has new option `--force` option (force update of HiveOS in situations when `selfupgrade` says "Hive is up to date" but this is not true)
*   WildRig-Multi v0.19.1 (added glt-globalhash, glt-hex algos, implemented GPUs monitoring)
*   CPUminer-opt v3.9.7 (new parameters for yescrypt/yespower algos - param-n, param-r, param-key)
*   T-Rex v0.13.0 (added tensority algorithm, added dedal algorithm back, added SSL support)
*   XMRig v2.99.4-beta (as replace for v2.99.1-beta: fixed compatibility with hwloc 1.10.x, optimized RandomX initialization and switching, fixed rare crash when re-initialize dataset)
*   CCminer-djm34 v1.2.0 (better handling of eventual packet losses)
*   *NEW* CCminer-xaya v0.1 (ccminer fork which support neoscrypt-xaya algo)
*   *NEW* TT-Miner 3.0.0 (Nvidia miner supported algos: Ethash,Lyra2Rev3,MTP,Myr-Gr,ProgPoW variants,TetHashV1,UbqHash)

##### 0.6-59@190802 2019-08-02
*   NanoMiner v1.5.3 (fixed issue with Nvidia devices not shown on nanominer -d output)
*   CCminer v3.9.6.2 (added new algo blake2b, faster myr-gr on Ryzen using SHA, faster blake2s SSE2, small speedup of around 1% for several other algos)
*   XMRig fork: XMRigCC v1.95 (integrated algos: cn-conceal, argon2-512 "chukwa", argon2-256 "chukwa-wrkz")
*   XMR-Stak 2.10.7 (fixed Nvidia critical bug, optimize VEGA auto suggestion, removed unsupported currencies: turtlecoin, xcash, loki)

##### 0.6-59@190730 2019-07-30
*   Nvidia OC fix for GTX 16xx and RTX 20xx cards (still no fan control for RTX)
*   Bminer v15.7.6 (improved the performance of the miner of Cuckatoo31, increased the dynamic ranges of -intensity)
*   PhoenixMiner v4.5c (fixed issue with ProgPOW BCI mining on Nvidia RTX20x0 and GTX16x0 cards)
*   CCminer-djm34 v1.1.26 (stability improvement: rearrange how the cards are assigned to thread)
*   XMRig v2.99.3-beta (as replace for v2.99.1-beta: fixed hwloc auto configuration on AMD FX CPUs, added NUMA support via hwloc, fixed miner freeze when switch between RandomX variants, fixed dataset initialization speed. Notice: since this is a beta version, you must directly select the v2.99.1-beta of the miner in the flight list / miner settings)

##### 0.6-58@190725 2019-07-25
*   Gminer v1.53 (improved performance for EQ 144/5 and 192/7 on RTX cards)
*   CCminer-djm34 v1.1.25 (stability improvement)
*   CCminer-enemy/Z-Enemy v2.1 (performance improvements: +4-5% most algos: x16r/x16s/x17/hex/bitcore/bcd)
*   XMRig v2.99.1-beta (added randomx/loki support. Notice: since this is a beta version, you must directly select the version of the miner in the flight list / miner settings)

##### 0.6-58@190724 2019-07-24
*   Bminer v15.7.4 (improved performance cuckaroo29d/AE, added 4G solver for cuckaroo29d)
*   SGminer-djm34 v0.1.2 (improved hashrate)
*   CCminer-djm34 v1.1.24 (better handling pool connection, solve various crash problem due to pool sending empty data, sliglty improved speed on 20x cards)
*   ETHminer v0.18.0 (Release, CUDA 10.0 build)
*   Fixed issue XMR-Stak v2.10.6 with stable image

##### 0.6-58@190722 2019-07-22
*   Bminer v15.7.3 (improved performance cuckaroo29d)
*   XMR-Stak v2.10.6 (fix cryptonight_v8 and derived pows)

##### 0.6-58@190721 2019-07-21
*   TeamRedMiner v0.5.6 (MTP algo improvements up to +3%)

##### 0.6-58@190720-2 2019-07-20
*   XMRig: some cleanup and reduced default devfee to 1%
*   XMRig-SChernykh: fixed syntax of global config file

##### 0.6-58@190720 2019-07-20
*   CPUminer-opt v3.9.6.1 (added new algos: x21s, hex)
*   Bminer v15.7.2 (related to cuckaroo29d: improved the stability, reduced the CPU usage, added 5G solver)
*   Gminer v1.52 (improved performance for EQ 144/5 and 192/7 on RTX cards)
*   PhoenixMiner v4.5b (improved stability of Nvidia kernels, added support latest AMD drivers up to v19.30, added advanced hardware monitoring, increased the maximum supported DAG epoch to 450, fixed the devfee pools for some of the alternative coins)
*   XMRig v2.16.0-beta (added support RandomWOW, please select version in FS/miner config)
*   NEW XMRig-SChernykh v2.15.4-beta2 (as xmrig fork schernykh, for RandomWOW algo)
*   Claymore's Dual ETH Miner - fixed DAG loading on AMD 4G cards for ETC/ETH when GUI enabled

##### 0.6-58@190718 2019-07-18
*   CPUminer-opt v3.9.6 (added algos: bmw512, x16rt, x16rt-veil, x13bcd)
*   NanoMiner v1.5.2 (fixed Cuckarood29 issue on AMD)
*   NBMiner v24.2 (fixed Cuckarood29 autoswitch)
*   Bminer v15.7.1 (improved Cuckaroo29d algo)
*   GrinGoldMiner v3.0 (CPU&CUDA updated PoW hardfork to Cuckarood29)
*   GrinMiner v2.0.0 (added support GRIN hardfork to cuckarood29 algo)

##### 0.6-57@190716-2 2019-07-16
*   lolMiner v0.8.5 (added support Grin29 hardfork for AMD 4G/8G cards: use GRIN-AD29)
*   NBMiner: workaround for v24.1 with GRIN-29 hardfork

##### 0.6-57@190716 2019-07-16
*   CPUminer-opt v3.9.5.4 (fixed hodl with aes-sse42, fixed sha256q with avx2, fixed skein2 buffer overflow)
*   Gminer v1.51 (added support Grin29 hardfork to Cuckarood29: use grin29 for autoswith to new algo, added BeamHashII algo for BEAM hardfork: use beamhash to autoswitch to new algo)
*   NBMiner v24.1 (added support Grin29 hardfork, improved performance on Grin29 & AE, added support for mining SERO)
*   lolMiner: fix displaying Zel.Cash algo EQ 125/4 in dashboard

##### 0.6-57@190710 2019-07-10
*   Fixed `hssh` for PXE boot
*   TeamRedMiner v0.5.5 (added cuckatoo31 algo for grin; v0.5.4: fixed API bug for MTP, small MTP improvements)
*   lolMiner v0.8.4 (fixed a 0 sol/s issue for ZEL, reduced EQ 125/4 memory usage to 2.9G, fixed a bug with the stratum for 125/4, 144/5, 192/7 and 96/5 in case the pool sends a very low job id)
*   RHminer v1.5.3 (added internal cpu throttlin, fixed duplicate shares)
*   nanominer v1.5.0 (added support for Grin's upcoming hardfork to Cuckarood29 algo, added support 6G+ Nvidia on Cuckaroo29/Cuckarood29, improved randomhash)
*   Sushi Miner (CUDA/OCL): fixed stats
*   CryptoDredge: fix config generation

##### 0.6-56@190705 2019-07-05
*   Gminer v1.50 (fixed performance regression for BEAM)
*   CryptoDredge v0.20.2 (improved argon2d-nim, improved x16-like algos, bug fixes)

##### 0.6-56@190704 2019-07-04
*   Gminer v1.49 (fixed bug in v1.48 with Beam mining on GTX 1060 3GB, improved in v1.48 performance for EQ 150/5 and EQ 125/4 algorithms on RTX cards)
*   TeamRedMiner v0.5.3 (added support of MTP algo, small stabilization fixes for CN variants)
*   miniZ - fixed config generation

##### 0.6-56@190703 2019-07-03
*   fixed `nvidia-info` tool (added current PL and fixed displaying default PL)
*   nanominer v1.4.1 (fixed SSL connection with miningpoolhub, fixed calling amdmemtweaktool)
*   NEW SeroMiner v0.3.0 (as ethminer fork)
*   miniZ v1.4o (added support for 125/4 and added for testing 210/9)
*   CPUminer-opt v3.9.5.1 (improved log color scheme)
*   lolMiner v0.8.3 (added 16 GByte solver for Cuckatoo31)
*   CCminer-djm34 v1.1.23 (stability improvement)
*   T-Rex v0.12.1 (improved MTP by 1-3% on some cards)
*   Gminer - fixed broken stats on some systems

##### ASIC 0.1-12 2019-06-26
*   Initial support of Antminer S17, S17 Pro, T17
*   Antminer Z11
*   Antminer L3 customs, T9 customs
*   Traffic stats optimization
*   Initial support (beta) for Innosilicon T3
*   Bulk install updates
*   Antminer S9 customs fix
*   Selfupgrade fixes

##### 0.6-55@190626 2019-06-26
*   nanominer v1.4.0 (added 'memTweak' option to control AMD GPU memory timings on Ethash algo, faster Ethash kernel on Vega/VII GPU)
*   Sushi Miner CUDA v2.1.1 (hashrate improvement and minor bugfixes)
*   CPUminer-opt v3.9.5 (new share reporting information scheme)
*   lolMiner v0.8.2 (added support for ZelHash for upcoming July 02 hardfork of ZEL)
*   CCminer-djm34 v1.1.22 (solved issue which were causing lost of connection and/or connection with pool)
*   WildRig-Multi v0.17.9 (fixed blake2b family, wildkeccak around 1% speed increase)

##### 0.6-55@190622 2019-06-22
*   renamed tool to change rig name from "workername" to `wname`
*   fixed processing of reboot flag in batch mode for AMD cards
*   Gminer v1.47 (significant performance improvements for VDS)
*   WildRig-Multi v0.17.8 (lower power consumption on pre-Vega GPUs and higher hashrate on Vega GPUs)
*   KBminer v1.3.11 (bug fix release)

##### 0.6-54@190619 2019-06-19
*   added new tool `workername` to change rig name
*   minor linux fixes
*   CPUminer-opt v3.9.4 (faster AVX2 for lyra2v3, quark, anime; fixed skein AVX2 regression)
*   CCminer-djm34 v1.1.20 (hashrate improvement up to 5%, bug fixes)
*   Gminer v1.46 BETA (added ZelCash Equihash 125/4, improved Grin29/Swap/AE)
*   Sushi-Miner-CUDA v2.1.0 (improved performance)
*   WildRig-Multi v0.17.7 (slightly improved different algorithms for Vega cards)

##### 0.6-53@190618 2019-06-18
*   T-Rex v0.12.0 (added honeycomb algo)
*   WildRig-Multi v0.17.6 (added skein2 algo, up to 6% faster blake2b-btcc and blake2b-glt)

##### 0.6-53@190617-2 2019-06-17
*   KBminer: fixed startup with NVidia's backend enabled builds

##### 0.6-53@190617 2019-06-17
*   Claymore's Dual ETH v14.7 (no new features in Linux build, bug fixes)
*   KBminer v1.3.10 (added support mining vds on Nvidia cards)

##### 0.6-52@190614 2019-06-14
*   TeamRedMiner v0.5.2 (bug fix release without new features)
*   CPUminer-opt v3.9.3.1 (fixed x16r algo 25% invalid share reject rate, fixed a couple of regressions)
*   NBminer v23.3 (fixed mining CuckooCycle on NiceHash)
*   KBminer v1.3.8 (improved vds performance by 25%, reduced hashrate lose in pools, notice: build only supports VDS on AMD cards)

##### 0.6-52@190613 2019-06-13
*   Update URL for Intel e1000e driver
*   Fixed `hello` fail for some types net-interfaces
*   Improved support of Push Interval (interval will decreased if sending stats error occurred)
*   XMR-Stak v2.10.5 (up to 10% improvement for cn-gpu on Nvidia)
*   KBminer v1.3.3 (up to 10% on vds, notice: version only supports VDS on AMD cards)
*   WildRig-Multi v0.17.5 (added blake2b, blake2b-glt, blake2s algos)

##### 0.6-51@190609 2019-06-09
*   Fixed AMD OC on mixed rigs
*   CPUminer-opt v3.9.2.4 (yet another cpu-affinity fix)
*   T-Rex v0.11.1 (significant x25x speed increase, many bug fixes)
*   Claymore's ETH Dual: fixed stats when mining stopped by overheating on some GPU

##### 0.6-50@190607 2019-06-07
*   Fixed an issue with AMD OC, which appeared in v0.6-49 on some configurations
*   CCminer-KlausT v8.25 (added lyra2v3, bug fixes)
*   TeamRedMiner v0.5.1 (added better support for CN intensities 16*15, better support x16rt, fixed some issues)

##### 0.6-49@190606 2019-06-06
*   Added LA watchdog & GPU hang detection
*   CPUminer-opt v3.9.2.3 (cpu-affinity fix)
*   KBminer v1.3.0 (added vds algo, build only for AMD platform)
*   TeamRedMiner v0.5.0 (added x16-like algos support: x16r, x16s, x16rt; added new cn-like algos: heavy, haven, saber)

##### 0.6-48@190605 2019-06-05
*   CPUminer-opt v3.9.2.2 (added sha256q algo, code optimizations on some algos)
*   WildRig-Multi v0.17.4 (added anime algo, improved honeycomb up to 3%)

##### 0.6-48@190603 2019-06-03
*   CryptoDredge v0.20.1 (fixed too many rejected shares on MTP algo, improved argon2d algos)
*   nanominer v1.3.4 (fixed critical connection issue introduced in version 1.3.3)

##### 0.6-47@190601 2019-06-01
*   Added support for diskless rig
*   CPUminer-opt v3.9.1.1 (added sonoa algo, fixed non-avx2)
*   nanominer v1.3.3 (fixed random Monero mining crashes on some connection types)
*   SGminer-fancyIX v5.6.1.3.b6 (added x25x algo support)
*   Gminer v1.45 (improved performance for Grin29/AE/SWAP on Nvidia cards)
*   XMRig /-AMD/-Nvidia v2.14.4 (removed obsolete automatic variants)
*   WildRig-Multi v0.17.3 (up to 20% faster x25x)

##### 0.6-46@190528 2019-05-28
*   Claymore's Dual ETH v14.6.1 (fixed hashrate drops on Nvidia cards vs v12.0)

##### 0.6-46@190527 2019-05-27
*   Claymore's Dual ETH v14.6 (first v14.x series Linux build, options -rxboost and -strap not working in Linux build)
*   CryptoDredge v0.20.0 (improved MTP algo, improved argon2d algo, new argon2d-nim algo)
*   WildRig-Multi v0.17.2 (fixed support x22i and x25x algos, re-tuned auto parameters for Baffin)
*   ccminer-enemy v2.0 (known as z-enemy miner)
*   NEW ccminer-rfv2 v1.0.2 (ccminer fork for Rainforest v2)

##### 0.6-45@190525 2019-05-25
*   added support of RXboost feature (fine tuning memory timings for Polaris cards)
*   Gminer v1.44 (improved GPU utilization for high-end GPUs on VOLLAR)
*   WildRig-Multi v0.17.0 (added x25x, re-tuned auto-parameters to maximize hashrate)
*   GrinPro v2.2 (fixed AMD compatibility)

##### 0.6-44@190522 2019-05-22
*   updated `amdmemtweak` v0.1.8.1
*   fixed teominer for AMD platform

##### 0.6-43@190521-2 2019-05-21
*   Nanominer v1.3.2 (fixed hanging while enumerating AMD devices on some systems)

##### 0.6-43@190521 2019-05-21
*   `hive-replace` fixed md5 checksum check
*   fixed time synchronization
*   minor changes in AMD OC
*   WildRig-Multi v0.16.5 (better stability for wildkeccak using --scratchpad-safe-update on some systems, small improvements x16-like algo and honeycomb)
*   Nanominer v1.3.1 (fixed cn-r runtime compilation issue on some AMD devices)
*   cpuminer-opt v3.9.0 (added lyra2rev3/yespower/yespowerr16/phi2)
*   T-Rex v0.11.0 (added x25x algo, bug fixes with built-in watchdog)
*   Gminer v1.43 (added support for mining mining V-Dimension, added support AE for NiceHash)
*   NEW teominer v0.16.3 (ethminer fork for TEO Project)

##### 0.6-42@190515-2 2019-05-15
*   fixed T-Rex v0.10.2 restarts

##### 0.6-42@190515 2019-05-15
*   CryptoDredge v0.19.1 (fixed some issues)
*   WildRig-Multi v0.16.3 (honeycomb optimization, little improvements for x16-like algos, some special improvements for Vega)
*   nanominer v1.3.0 (added support cn-r and cn-rwz for AMD, improved QuarkChain support)
*   rhminer v1.5.1 (little performance boost)
*   T-Rex v0.10.2 (added mtp algo)

##### 0.6-41@190510-2 2019-05-10
*   NBMiner v23.2 (hotfix: fixed support AE for NiceHash)
*   WildRig-Multi v0.16.2 (fixed xevan on Vega, small improved x16-like algo)

##### 0.6-41@190510 2019-05-10
*   Gminer v1.42 (improved performance for BEAM at RTX cards, fixed performance regression on GTX 1080ti)
*   NBMiner v23.2 (improved Grin/AE/SWAP performance, added support AE for NiceHash)
*   WildRig-Multi v0.16.1 (added xevan algo, small improved speed at x16-like algos)

##### 0.6-40@190506 2019-05-06
*   Improved SSL session agent support
*   Added `Push interval` and `Maintenance mode` support
*   Added NVflash utility
*   Gminer v1.41 (improved performance for BEAM on Nvidia cards)
*   Bminer v15.5.3 (another fix invalid shares ETH+VBK when using multiple cards)
*   CryptoDredge v0.19.0 (added argon2d 250/4096 algos, improved mtp up to 5%, improved CN-like and cn-gpu, removed some old algos)
*   **NEW** miniZ v1.3n5 (fast and friendly Equihash 144/5, 150/5, 192/7, 96/5 CUDA miner)
*   Wildrig-Multi v0.16.0 (added wildkeccak, up to 5% honeycomb, some hashrate improvemnets x16-like algorithms)
*   Fixed Custom miner downloading from SSL resources (Bleeding Edge/VEGA images)

##### LINUX IMAGE RELEASE 0.6-39 2019-05-03
*   Release of stable branch with updating system packages, etc 
*   Updated Nvidia drivers to v418.56

##### 0.6-39@190501 2019-05-01
*   fixed wifi startup
*   bminer v15.5.2 (fixed invalid shares ETH+VBK)
*   gminer v1.40 (performance improvements for BEAM)

##### 0.6-38@190430 2019-04-30
*   stats traffic optimization
*   xmrig forks xmrigcc and xmrigcc-amd v1.9.3  (added cn-upx2 support)
*   nanominer v1.2.4 (QuarkChain support optimization and bug fixes)
*   teamredminer v0.4.5 (added cn-upx2 support)

##### 0.6-37@190426 2019-04-26
*   fixed disabling wifi service
*   nanominer v1.2.3 (fixed issue with devices parameter ignored for Ethash)
*   gminer v1.39 (added 4G solver AE, improved performance for 144/5, 192/7, Grin29, Swap, AE)

##### 0.6-36@190425 2019-04-25
*   bminer v15.5.1 (fixed regression Grin29 on RTX cards, huge hashrate improvements ETH+VBK)
*   nanominer v1.2.2 (added QuarkChain node support, up to 8% Grin29 for AMD RX580 8G)
*   HSPMinerAE v2.2.4 (hashrate improvements, improved stability, bug fixes)

##### 0.6-36@190424-3 2019-04-24
*   wildrig-multi v0.15.6 preview (honeycomb algo up to 30% faster)

##### 0.6-36@190424-2 2019-04-24
*   fixed packages dependencies

##### 0.6-35@190424 2019-04-24
*   fixed `amdmeminfo` tool

##### 0.6-34@190423-3 2019-04-23
*   bug fix

##### 0.6-33@190423-2 2019-04-23
*   fixed `selfupgrade`

##### 0.6-32@190423 2019-04-23
*   added OC support **Nvidia GTX 1660 TI** (need driver v418.43+)
*   added support **AMD Radeon VII** (VEGA's image)
*   updated `amdmemtweak` v0.1.7.1
*   updated some system tools
*   teamredminer v0.4.4

##### 0.6-31@190418 2019-04-18
*   updated `amdmemtweak` v0.1.7
*   lolminer v0.8.1 (added support for Grin31 4G/8G, stratum bug fixes 144/5, 192/7 and 96/5, improved general stability)
*   wildrig-multi v0.15.5 preview (added support honeycomb algo - BeeNode coin)
*   noncepool-amd and noncepool-nvidia v1.27 (fixed for bug when running 8+ days of uptime)
*   grinpro v2.1 (added swap support for AMD, a lot of improvemets and bug fixes)
*   nanominer v1.2.1 (fixed bug with crash on some system wititout Nvidia cards)
*   removed webchain fork of xmrig/-amd/-nvidia due Webchain coin hardfork to other algo
*   fixed ccminer-djm34 v1.1.16 and v1.1.17 packages
*   fixed nanominer randomhash algo stats

##### 0.6-30@190416 2019-04-16
*   improved `hssh`
*   improved `selfupgrade`
*   minor fixes
*   nbminer v22.3 (lower CPU usage on default settings when mining Grin & AE, improved Grin31 performance on 1080ti & 2080ti)
*   ccminer-djm34 v1.1.17 (adjusted default intensity to 20, fixed stratum/block/share difficulty)
*   bminer v15.5.0 (improved the performance Grin29, added dual-mining ETH+VBK)
*   fixed nanominer stats

##### 0.6-29@190412 2019-04-12
*   update `amdmemtweak` to v0.1.6
*   nbminer v22.1 (added Swap, improved Grin29/AE performance)
*   nanominer v1.2.0 (added Grin29 for 8G+ AMD cards, added cn-rwz for Nvidia, introduced new switching scheme to devfee)
*   gminer v1.37 (replaced v1.37 Beta, added 192/7 solver for AMD)
*   gminer v1.38 (added 4GB solver for Grin29 and Swap)

##### 0.6-28@190408 2019-04-08
*   fixed `nvidia-driver-update` broken by previous release
*   fixed hive-agent to work properly with new AMD flasher and 10+ cards
*   noncepool-amd and noncepool-nvidia v1.26
*   gminer v1.37 BETA as user selectable version (added 5GB solver for Grin29/Swap/AE, added 144/5 solver for AMD cards, added auto-switching to main pool from failover pool)

##### 0.6-27@190407 2019-04-07
*   NEW `nvstop` - tool for complete and correct unloading Nvidia drivers
*   improved nvidia-driver-update
*   updated AMD BIOS flasher to v4.50 (added support for Lexa and Vega)
*   NEW EggMinerGPU v4.00.100 (miner for Busmuth coin for eggpool)
*   NEW Noncepool-AMD v1.24 and Noncepool-Nvidia v1.24 (miners respectively AMD/Nvidia for Busmuth coin for noncepool)
*   fixed lolminer stats for Nvidia cards
*   fixed xmrig-amd-xmrigcc package
*   fixed xmrig-nvidia-fruityminer package

##### 0.6-26@190403 2019-04-03
*   update net-test tool (added msk.hiveos.farm host)
*   update hive-libs (added openssl 1.1.1b, cudart 10.1)
*   nbminer v21.4 (improved Grin31 performance, improved performance of Grin29 & AE on RTX cards)
*   cryptodredge v0.18.0 (add argon2d-dyn support, add NH support MTP and Grin29, add 2G solver for AE, add 4G solver for Grin29)
*   xmr-stak v2.10.4 (fixed CUDA bug on cn-r algo)
*   xmrig-nvidia v2.14.3 (fixed CUDA bug on cn-r algo)
*   NEW XMRig forks (XMRigCC, Hycon, Webchain) 
*   NEW XMRig-AMD forks (XMRigCC, Hycon, Webchain) 
*   NEW XMRig-Nvidia forks (Fruityminer, Hycon, Webchain) 
*   FIX rollback wildrig-multi to v0.15.4 p15 due buggy p16 release

##### 0.6-25@190402 2019-04-02
*   wildrig-multi v0.15.4 preview 16 (optimize CPU usage and fix VEGA's hashrate on rainforest algo)

##### 0.6-25@190401 2019-04-01
*   hive-replace now can save openvpn and wifi settings
*   kbminer v1.2.2 (bug fix)
*   zilminer v0.4.01 (some optimizations)
*   fixed broken install ccminer-djm34 v1.1.16 CUDA 9.2 package
*   wildrig-multi v0.15.4 preview 15 (rainforest algo hashrate bump up to 60TH per RX570 with good enough CPU)

##### 0.6-23@190327 2019-03-27
*   fix: nvidia-driver-update in some cases couldn't unload nvidia kernel module
*   teamredminer v0.4.3 (added cryptonight-turtle, added support for running CN mining single-threaded)
*   ccminer-djm34 v1.1.15 (fixed solo mining, increased default difficulty to 21)
*   small fixes for miners stats (phoenixminer, ccminer, cryptodredge, zjazz-cuda)

##### 0.6-22@190321 2019-03-21
*   nbminer v21.3 (fixed lower local hashrate than previously version)
*   kbminer v1.2.1 (fixed hashrate issues of Grin31 on Nvidia 2080Ti)
*   wildrig-multi v0.15.4 preview 8 (huge hashrate increase for rainforest for ex. 33GH/s from RX570)
*   phoenixminer 4.2c (added new Nvidia kernels v3 for Pascal cards, fixed the slower DAG generation on Vega/Radeon VII)

##### 0.6-22@190317 2019-03-17
*   nbminer v21.2 (improved performance of Grin29/Grin31)
*   gminer v1.36 (decreased CPU usage upo 40%, added option to control GPU intensity)
*   teamredminer v0.4.2 (added algos cn-v8 half/dbl/rwz, cn-r cpu usage should decrease up to 70%)
*   xmr-stak-fireice-uk v2.10.2 (fixed OpenCL memory leak)
*   xmr-stak-indeedminers v2.10.2.1 (sync fireice-uk)
*   phoenixminer v4.2b (fixed issue with RTX20x0 and 1660ti, other small bug fixes)

##### 0.6-22@190314-2 2019-03-14
*   fix xmrig-amd v2.14.1 package (added missing file)

##### 0.6-22@190314 2019-03-14
*   wildrig-multi v0.15.4 preview 7 (hashrate increased up to x2 on rainforest algo)
*   xmrig-amd v2.14.1 (fixed memory leak, autoconf for cn-r algo)
*   nbminer v21.1 (improved Grin29, added support RTX for Grin and AE, less rejected shares on NH, other fixes)

##### 0.6-22@190313 2019-03-13
*   wildrig-multi v0.15.4 preview 6 (less power consumption and slightly higher hashrate on rainforest algo)
*   nanominer v1.1.1 (fixed API stats)
*   phoenixminer v4.2a (new features including ProgPow BCI mining support, Etherrium stratum 2.0 support and many more and bug fixes)
*   rhminer v1.4 (various bug fixes)
*   kbminer v1.2 (up to 200% hashrate boost on Grin31)

##### 0.6-22@190312 2019-03-12
*   bminer v15.3.1 (slightly improved Grin29/31, reduced CPU usages on Grin31, fixed Grin29 regression on RTX cards, fixed Ethash speed reporting fix)
*   wildrig-multi v0.15.4 preview 5 (another improvements for rainforest algo up to 30%)
*   xmr-stak-fireice-uk v2.10.1 (Big Bug fix release: fixed cryptonight_r, cryptonight_gpu, masari; added cryptonight_v8_double)
*   teamredminer v0.4.1 (Big Bug fix release)

##### 0.6-22@190310 2019-03-10
*   bminer v15.3.0 ( improved the performance of Cuckaroo29 by 5% and slightly improve the performance of Cuckatoo31)
*   wildrig-multi v0.15.4 preview 4 (fix work on old CPUs,  improvements for rainforest algo up to 10%)
*   xmrig-nvidia v2.14.1 (bug fix)

##### 0.6-22@190309 2019-03-09
*   NEW kbminer 1.1.1 (AMD/NVidia AE/Grin29/Grin31 miner)
*   NEW nanominer 1.1.0 (ethash, cn-v8, cn-r miner)
*   NEW rhiminer v1.3 (randomhash cpu miner)
*   wildrig-multi v0.15.4 preview 3 (huge improvements for rainforest algo)
*   teamredminer v0.4.0 (added cn-r support, various improvements and bug fixes)
*   FIX xmr-stak v2.10.0 rebuild

##### 0.6-22@190308 2019-03-08
*   xmrig v2.14.1 (bug fix)
*   xmr-stak v2.10.0 (support hardforks of Monero and GRAFT)

##### 0.6-22@190307 2019-03-07
*   gminer v1.35 (improved Grin29/SWAP, added support AMD for Grin29/SWAP/AE)
*   xmrig, xmrig-amd, xmrig-nvidia 2.14.0 (added cn-rwz, cn-zls, cn-double)
*   fix AMD backend for xmr-stak v2.9.0

##### 0.6-22@190306 2019-03-06
*   nvidia-driver-update - fixed unload previous driver module
*   lolMiner v0.7.1 (updated kernels for MNX, added BEAM binary kernels for ROCm driver with --asm parameter)
*   nbminer v21.0 (added support for AE, improved performance on Grin29/31)
*   bminer v15.2.0 (improved performance on Grin29/31, reduced chance for rejected and stale shares for Grin 29/31, added support RTX 2080/2070)
*   xmr-stak-fireice-uk v2.9.0 (added cn-r algo for upcoming Monero hardfork)
*   wildrig-multi v0.15.4-preview (added rainforest algo, not set as default version, maybe buggy version)

##### 0.6-21@190302 2019-03-02
*   nvidia-info - fixed output of default PL 
*   amd-info - added output of VEGA's voltage
*   bminer v15.1.0 (improved performance of Grin29/Grin31)
*   xmrig v2.13.1 (optimized software AES)
*   ccminer-djm34 v1.1.14 (stability improvement, small hashrate bump)
*   ethminer v0.17.1 Release (set as Latest)
*   ethminer v0.18.0-rc.0 (add for testing)
*   grinprominer - fix miner uptime in stats
*   zilminer - rebuild v0.2.20 CUDA 9.2 package

##### 0.6-20@190225 2019-02-25
*   improved amd-info, nvidia-info tools
*   bminer v15.0.2 (improve fidelity of Cuckaroo29 on 1060/P106/1070)
*   lolMiner v0.7 release (add BEAM tuned kernel, change SAFE and add VDL on 192/7,  many other changes)
*   nbminer: fix config generation for tensority with empty intensity

##### 0.6-19@190224-2 2019-02-24
*   HOTFIX - fixed miners install system

##### 0.6-18@190224 2019-02-24
*   gpus-stat - PL will be used for Nvidia cards if power consumption not available from driver.
*   nbminer v20.0 (added Grin31 support, NH support for Grin)
*   xmrig, xmrig-amd, xmrig-nvidia v2.13 (added support cn-r, fixed cn-pico hashrate drop)
*   grinpro v1.20 (up to 30% faster on NVidia, reduced CPU usage)
*   gminer v1.34 (added support Swap coin)
*   zilminer v0.2.20 (new args for cmdline, small improvements)

##### 0.6-17@190219 2019-02-19
*   gminer v1.33 (improved performance for Grin-C29/AE)

##### 0.6-16@190218-2 2019-02-18
*   hive agent bug fix (update is highly recommended)
*   sgminer-djm34 v0.1.1 (duplicate shares fix)

##### 0.6-15@190217 2019-02-17
*   bminer 15.0.0 (add support 8G cards on cuckatoo31)
*   cryptodredge 0.17.0 (add cn-gpu, cn-trtl, aeternity, cuckroo29, fix cn-fast2)
*   xmr-stak-fireice-uk v2.8.3 (implement Ryo fork, add cn_conceal algo)

##### 0.6-15@190216 2019-02-16
*   hssh - fixes and improvements
*   NEW nvidia-info - new console tool for NVidia GPUs (like amd-info)

##### 0.6-14@190214 2019-02-14
*   Hive agent refactoring - prevents workers from wents to "offline" when longtime commands executed from web interface
*   xmrig, xmrig-amd, xmrig-nvidia 2.12.0 (added cn-wow, improved cn-gpu)
*   sgminer-djm34 0.1.0 (improved mtp)
*   sgminer-fancyix 5.6.1.3.b5ip3 (improved mtp)
*   zilminer 0.2.13

##### 0.6-13@190212-2 2019-02-12
*   xmr-stak-fireice-uk: fix update issue

##### 0.6-13@190212 2019-02-12
*   bminer v14.3.1 (improved Grin-C29, reduced rejects on Grin-C31 add support NH for Grin-C29/C31)
*   wildrig-multi v0.15.3.8 (tuned auto parameters for VEGAs)
*   xmr-stak-fireice-uk v2.8.2 (improved cn-gpu, add new coins)
*   xmrig-amd v2.11.1 (fixed TRTL)
*   NEW! zjazz-cuda v1.2 (Cuckoo PoW: Merit, BitCash)

##### 0.6-13@190210-2 2019-02-10
*   Hive Shell Beta (hssh) - fixed issue with some installations based on some old or beta images
*   bminer v14.3.0 (improve Grin-C31)
*   wildrig-multi v0.15.3.7 (tuned auto parameters for RX550)
*   xmrig, xmrig-amd, xmrig-nvidia v2.11.0 (add cn-gpu)
*   lolMiner v0.7 alpha 5b (small bug fix)
*   sgminer-djm34 v0.0.7 (improved mtp)
*   sgminer-fancyix v5.6.1.3.b5ip2 (improved mtp)
*   sgminer-fancyix: fix HW monitoring

##### ASIC 0.1-11 2019-02-08
*   Autotune for S9 (Hiveon firmware)
*   power and share monitor for S9 (Hiveon firmware)
*   Antminer S11
*   Antminer DR3
*   Zig Z1/Z1+ (some firmwares)
*   Z9 Efudd firmware
*   Innosilicon new firmware fix
*   ipscan for netinstall (antminer)
*   netinstall fix


##### 0.6-12@190207-3 2019-02-07
*   fix Hive Shell Beta - removed dependency on library download
*   ccminer-tpruvot 2.3.1 (fixed broken binary)
*   wildrig-multi 0.15.3.6 (bug fixes)
*   gringoldminer 2.9a (some improvements for AMD and CPU usage)

##### 0.6-11@190207 2019-02-07
*   NEW! Hive Shell Beta - teleconsole replacement tool
*   bminer 14.2.0 (added Grin-C31 for 1080ti)
*   ccminer-tpruvot 2.3.1 (added lyra2rev3, sha256q, exosis, blake2b)
*   wildrig-multi 0.15.3.5 (bug fixes)
*   lolMiner 0.7 alpha 5 (added NH support)
*   NEW! HSPminerAE 2.0.7 (AE CUDA miner)

##### 0.6-10@190206 2019-02-06
*   gminer 1.31 (improved grin29, aeternity; added grin31)
*   wildrig-multi 0.15.3.2 preview (added bmw512)
*   sgminer-fancyix 5.6.1.3.b5ip1
*   sgminer: fixed config generation

##### 0.6-10@190204 2019-02-04
*   cryptodredge 0.16.2 (fix lyra2rev3, x16rt; added CNFastv2 and CNSuperFast)
*   teamredminer 0.3.10 (added lyra2rev3 support)
*   gminer 1.28 (fix NH for Beam, add NH for Grin29)
*   t-rex 0.9.2 (fix x16rt for GIN)
*   xmr-stak-fireice-uk 2.8.0 (add cn-gpu, cn-trtl)
*   xmr-stak-indeedminers 2.7.1
*   sgminer-djm34 0.0.6_mtp (Zcoin OCL official miner)

##### 0.6-10@190201-3 2019-02-01
*   wildrig-multi 0.15.2.2 (bug fix)

##### 0.6-10@190201-2 2019-02-01
*   sgminer-fancyix 5.6.1.3.b5i (added mtp support)
*   wildrig-multi 0.15.2.1 (fixed lyra2REv3, x16rt, implemented auto tunnig)

##### 0.6-10@190201 2019-02-01
*   NEW zilminer 0.1.25 (added as ethminer fork for mining Zilliqa)
*   added autoconfiguration for all cards in a rig if no user config defined (grinminer, grinpro, gringoldminer)

##### 0.6-10@190130 2019-01-30
*   gminer 1.25 (Added aeternity, fixed BEAM for nicehash)
*   nbminer 14.0 (Improved BTM, GRIN mining speed)
*   bminer 14.1.0 (Fixed BEAM for nicehash, improved AE, GRIN mining speed)

##### 0.6-10@190129-2 2019-01-29
*   NEW [NBminer](https://github.com/NebuTech/NBMiner) 13.2.0
*   NEW [GrinPro Miner](https://grinpro.io) 1.1

##### 0.6-10@190126 2019-01-26
*   lolMiner 0.7 alpha 4 (improved memory usage and stability)
*   cast-xmr 1.7.0

##### 0.6-10@190125-3 2019-01-25
*   bminer package bugfix

##### 0.6-10@190125-2 2019-01-25
*   gminer 1.23 (improved performance and optimized memory usage for GRIN)
*   bminer 13.2.0 (reduce rejected shares on C29)
*   minor fixes

##### 0.6-10@190124 2019-01-24
*   lolMiner 0.7 alpha 3 (added 3G kernel for BEAM)
*   sgminer-faincyix 5.6.1.3.b5hp1 (added argon2d)
*   xmrig, xmrig-amd, xmrig-nvidia 2.10.0 (added cn-pico)

##### 0.6-10@190123 2019-01-23
*   gminer 1.22 (improved performance and optimized memory usage for GRIN)
*   bminer 13.1.0 (add support mining GRIN/AE with mining cards P104-100)

##### 0.6-10@190122-2 2019-01-22
*   gminer 1.21 (+25% hashrate and improve stability on GRIN C29)

##### 0.6-10@190122 2019-01-22
*   bminer 13.0.0 (reduced rejected shares, +30% hashrate on GRIN C29, AE)
*   lolMiner 0.7 alpha 2b (fixed reconnection bug)
*   xmrig, xmrig-amd xmrig-nvidia 2.9.4 (fixed MSR support)
*   ethminer 0.17.0 Release (replace rc2 and set as Latest version)
*   grinminer: fixed and improved stats

##### 0.6-10@190120 2019-01-20
*   gminer 1.20 (reduced CPU usage)
*   bminer 12.2.0 (reduced CPU usage, fix issues with some pools)
*   gringoldminer 2.8b (added support cards with 6G VRAM)
*   lolMiner 0.7 alpha 2 (only BEAM, select version directly)
*   gringoldminer: enabled TLS support
*   grinminer: stats improvements for AMD cards
*   lolMiner: stats improvements on Overview page

##### 0.6-10@190117-2 2019-01-17
*   gminer 1.19 (added GRIN C29)
*   ccminer-djm34 1.1.13
*   phoenixminer 4.1c
*   grinminer (rebuild packages)

##### 0.6-10@190117 2019-01-17
*   NEW gringoldminer 2.7b
*   grinminer 1.0.2
*   bminer 12.1.0
*   xmrig, xmrig-amd, xmrig-nvidia 2.9.3
*   sgminer-fancyix 5.6.1.3.b5h

##### 0.6-10@190115 2019-01-15
*   bminer 12.0.1 (add support for GRIN)
*   cryptodredge 0.16.1
*   grinminer 0.5.2
*   sgminer-kl 1.0.9
*   fixed cast-xmr reported fans speed 

##### 0.6-10@190110 2019-01-10
*   gminer 1.18
*   beam-opencl-miner 1.0.63
*   phoenixminer 4.1a
*   bminer 11.4.0
*   ccminer-djm34 1.1.12 (cuda 9.2/10.0 packages)
*   wildrig-multi 0.15.1.3
*   sgminer-fancyix 5.6.1.3.b5gp3 (added lyra2zz)
*   improved miner stats on equihash 150/5 (gminer, beamcl)

##### 0.6-10@190107 2019-01-07
*   bminer 11.3.0
*   gminer 1.15
*   t-rex 0.9.1
*   wildrig-multi 0.15.1

##### 0.6-10@190106-2 2019-01-06
*   ccminer-djm34 1.1.10
*   cryptodredge 0.16.0

##### 0.6-10@190106 2019-01-06
*   Fixed system logs, they eated disk space even when they were tuned off

##### 0.6-09@190104 2019-01-04
*   bminer 11.2.0 (added aeternity and equihash 150/5 support)
*   wildrig-muilti 0.15.0 (build 12)
*   sgminer-fancyix 5.6.1.3.b5gp2

##### 0.6-09@190103 2019-01-03
*   wildrig-multi 0.15.0 (added x16rt, mtp)

##### 0.6-09@190101 2019-01-01
*   gminer 1.14

##### 0.6-09@181231 2018-12-31
*   gminer 1.13
*   ccminer-mtp 1.0.0 rebuild
*   ccminer-djm34 1.1.9
*   ccminer-suprminer 1.6
*   cryptodredge 0.15.2
*   sgminer-fancyix 5.6.1.3.b5gp1

##### 0.6-08@181229 2018-12-29
*   ccminer-mtp 1.0.0 by krnlx
*   cryptodredge 0.15.1

##### 0.6-08@181227 2018-12-27
*   disk-expand and swap-file fixed for running from dashboard
*   claymore 12.0
*   bminer 11.0.0 
*   fixed phoenixminer stats
*   other small fixes

##### 0.6-07@181222 2018-12-22
*   ccminer-djm34 1.1.3
*   ccminer-djm34 1.1.4 (latest)
*   gminer 1.12
*   finminer 2.4.7
*   other small fixes

##### 0.6-07@181219 2018-12-19
*   swap-file - utility for manage swap file
*   lolMiner 0.6 release
*   ethminer 0.16.2 (set as latest)
*   ethminer 0.17.0-rc2
*   t-rex 0.8.9
*   ccminer-djm34 1.1.1
*   ccminer-djm34 1.1.1-dev (rebuild for test2)
*   teamreaminer stats fix

##### 0.6-06@181215 2018-12-15
*   ccminer-djm34 1.1.1-dev
*   t-rex 0.8.8
*   ccminer-enemy 1.28 (z-enemy)
*   finminer 2.4.6
*   fixed avx2 support in cpuminer-opt
*   other small fixes

##### 0.6-06@181212 2018-12-12
*   lolminer package small fixes

##### 0.6-06@181211-5 2018-12-11
*   t-rex 0.8.6 fix cuda 10.0 package

##### 0.6-06@181211-4 2018-12-11
*   t-rex 0.8.6 fix cuda 9.2 package
*   xmr-stak version control fix

##### 0.6-06@181211-2 2018-12-11
*   xmr-stak 2.7.0 patch fixed issue with BitTube (same as v2.7.1)
*   ccminer-enemy 1.27 (known as Z-Enemy)
*   ccminer-djm34 1.1.0 (mtp algo support)
*   cryptodredge 0.14.0
*   sgminer-fancyix 5.6.1.3.b5f
*   wildrig-multi 0.14.0
*   t-rex 0.8.6
*   fixed version selection ccminer, xmr-stak, wildrig-multi
*   improved teamredminer stats (added hw report)
*   improved OC for AMD RX Vegas
*   For mtp algo you need 5G RAM per card on your rig and at least 5G free VRAM on GPU

##### 0.6-05@181204-4 2018-12-04
*   ccminer-enemy-1.26
*   finminer-2.4.4
*   lolminer-0.6.a4
*   t-rex-0.8.5
*   xmr-stak-fireice-uk-2.7.0
*   phoenixminer fix
*   ccminer-klaust-8.21-r17
*   ccminer-klaust-yescrypt-8.21-r17

##### 0.6-05@181202-2 2018-12-02
*   bminer 10.7.0
*   sgminer-fancyix 5.6.1.3.b5f
*   sgminer-gatelessgate 0.1.3-pre6b
*   cast-xmr 1.6.6

##### 0.6-05@181201 2018-12-01
*   phoenixminer 4.0b
*   gminer 1.10
*   finminer 2.4.3
*   wildrig-multi 0.13.4
*   cryptodredge 0.13.0
*   Minor fixes
 
##### 0.6-04@181129 2018-11-29
*   `hive-replace` supports SMB and NFS shares
*   phoenixminer 4.0a
*   t-rex 0.8.3
*   teamredminer 0.3.8, fixed 10+ gpus stats
*   cryptodredge 0.12.0
*   wildrig-multi 0.13.2
*   ccminer-enemy 1.25
*   xmr-stak 2.6.0
*   NEW: gminer 1.08
*   NEW: finminer 2.4.2
*   Fixed xmrigs for bittube 

##### 0.6-03@181124 2018-11-24
*   NEW: `hive-replace`, ultimate solution to replace Hive image on a running Linux system. 
You give URL where the image is (better on local network, HTTP, FTP, NFS or on local disk).
Script will write it to disk, will preserve existing rig.conf or ask for FARM_HASH.
You can run this script on any other linux (Ubuntu, Ethos, SMOS).
Updating system images with drivers and everything can't be easier now.
*   bminer 10.6.0
*   xmrig-amd 2.8.6
*   cryptodredge 0.11.0
*   Fixed broken HW watchdog scripts


##### 0.6-02@181122 2018-11-22
*   t-rex 0.8.0
*   wildrig-multi 0.13.1
*   ccminer-enemy 1.24.3
*   cast-xmr 1.6.0
*   sgminer-fancyIX 5.6.1.3.b5f (huge speedup on x22i algo)
*   Minor changes for HW watchdogs


##### 0.6-01@181121 2018-11-21
*   **DON'T UPGRADE TO THIS VERSION IF YOU DON'T WANT TO BE EARLY ADOPTER AND YOUR FARM UPTIME IS CRITICAL.**
This is a very big update with many changes. It was tested but usually there are hotfixes with such things.
*   Totally redesigned packages architecture. Now Hive Core and miners are in separate packages.
Updates are much quicker and traffic wise. Only required miners and updated. 
Miners are autoinstalled if you use them. 
You can have different miners versions installed without downgrading.
*   Version now consists of Hive Core version and repository update date. Like `0.6-01@181121`.  
So miners packages can be released without changing Hive Core version. 
Hive Core itself is the thing that contains all the scripts which control system boot, overclocking, watchdogs, etc. But not the miners. 
*   `hpkg` console utility to manually control Hive packages, uninstall, update, list, etc. Run it to see usage instructions.
*   Most of custom miners are in main branch now. Please update you Flight Sheets. 
*   NEW: cast-xmr
*   NEW: cryptodredge
*   NEW: ethminer ubiq
*   NEW: phoenixminer
*   NEW: sgminer fancyIX, kl
*   NEW: t-rex
*   NEW: teamredminer
*   NEW: wildrig-multi
*   NEW: xmrig-amd, xmrig-nvidia
*   bminer 10.5
*   optiminer deprecated and removed
*   ccminer-update deprecated, all miners are included now
*   CUDA 9.2 is now default for most miners. Nvidia driver >=396 is required. 
It is advised to use `nvidia-driver-update` on old installations. Or reflash Hive image.
Optionally you can select CUDA 9.1 or lower versions of miners if available.    
*   custom-get - no needed for `-f` for update, just change URL in FS
*   Updated version in `/hive/opt/e1000e/e1000e-upgrade.sh` to update Intel LAN driver 
*   One more HW watchdog on the same QinHeng HL-340 chip. 
`/hive/opt/qinheng/wd-fixorgua` to enable this type of WD. 
(Thanks to @webgkv for providing control sequences) 
*   Lot's of other small fixes and improvements


##### 0.5-82 2018-10-24
*   One more the latest final fix of shitty xmr-stak API hotfix which caused rig to go offline


##### 0.5-81 2018-10-23
*   One more xmr-stak API hotfix which caused rig to go offline


##### 0.5-80 2018-10-22
*   xmrig 2.8.3
*   Fixed xmr-stak stats which caused rig to go offline


##### 0.5-79 2018-10-20
*   New command `sreboot wakealarm` will shutdown and then boot after 30 seconds boot again, 
    useful when you need to poweroff
*   New command `netconf` wizard for network configuration, `netconf-set` CLI command to set network config for eth0 interface 
*   xmr-stak-fireice-uk-2.5.1


##### 0.5-78 2018-10-01
*   atiflash can now flash VBIOS for 10+ GPU
*   xmr-stak-fireice-uk-2.5.0
*   xmr-stak-indeedminers-2.5.0-beta
*   xmrig-2.8.1
*   ethminer 0.16.1
*   optionally run `nvidia-driver-update` to upgrade to 410.66 after updating hive, run this only if you know you need it


##### ASIC 0.1-10 2018-10-07
*   Antminer S9 VNISH firmware
*   Antminer S9J
*   Antminer S9 Hydro
*   Antminer T9
*   Antminer B3
*   Antminer S7
*   `asic-find` for Antminer, run `asic-find 5` and LEDs will blink for 5 seconds
*   Innosilicon cron commands to prevent memory leaks in stock firmware, `inno-reboot miner enable/disable`, `inno-reboot asic enable/disable`, `inno-reboot status`, check docs on git.
*   fixed watchdog after reboot


##### 0.5-77 2018-10-01
*   progpowminer cuda9.2 v16 final
*   ewbf zhash 0.6
*   amdmeminfo added detection of RX560
*   some miners now can report bus numbers of gpus, will you be used to report hashes in gpu table on web
*   fixed agent restart by cron


##### ASIC 0.1-09 2018-09-26
*   Innosilicon D9 DecredMaster
*   Innosilicon S11 SiaMaster
*   Antminer Z9
*   fix fan contol
*   fix api-groups
*   minor fixes
*   **IMPORTANT for Z9-MINI only** Don't use upgrade button. To update from previous version please run the following
`screen -dm -S selfupgrade bash -c 'cd /tmp && curl -L --insecure -s -O https://raw.githubusercontent.com/minershive/hiveos-asic/master/hive/bin/selfupgrade && sh selfupgrade'`

##### LINUX IMAGE RELEASE 0.5-76 2018-09-24
*   At the moment Hive provides "STABLE16" image based on Ubuntu 16 and "Bleeding Edge" based on Ubuntu 18
*   STABLE16: upgraded Nvidia drivers, system packages, etc.
*   Bleeding Edge: AMD drivers in linux kernel 4.15, OpenCL from 16.60


##### 0.5-76 2018-09-24
*   minor fixes
*   ccminer-enemy 1.21, use `ccminer-udpate` to update it
*   custom phoenixminer 3.5d
*   custom bminer 10.3.0
*   custom finminer to v2.2.2
*   fixed custom t-rex 0.6.6
*   fixed custom teamredminer 0.3.1
*   use `custom-get MINER_DOWNLOAD_URL -f` to upgrade custom miners


##### 0.5-75 2018-09-22
*   **REBOOT REQUIRED AFTER THIS UPDATE!**
*   IMPORTANT: default setting in claymore is "-allpools 0" now, 
maybe you will need to add "-allpools 1" to user config in Flightsheet if you use non-ETH pool. This can improve stability.   
*   progpowminer v16rc1 cuda9.2
*   amdmeminfo improved to report correct memory brand
*   added support for Chinese Arduino Nano Watchdogs, instructions [on forum](https://forum.hiveos.farm/t/chinese-watchdog/7615)
*   fixed CURL_OPENSSL_4 error on Ubuntu 18
*   Other minor fixes and refactoring


##### ASIC 0.1-08 2018-09-13
*   Bulk installation script, you can install Hive on all your ASICs in local network, check [usage instructions on Git](https://github.com/minershive/hiveos-asic).
*   Worker now report's it's unique ID. Required to restore worker with FARM_HASH only, no need for RIG_ID anymore.   
*   Minor fixes


##### 0.5-74 2018-09-12
*   ethminer progpow correct algo reporting
*   Fixed claymore restart on 13+ gpu rigs
*   Improved `selfupgrade` not to hang on dialogs, prevent upgrading whole Ubuntu
*   Worker now report's it's unique ID. Required to restore worker with FARM_HASH only, no need for RIG_ID anymore.   
*   Minor fixes


##### 0.5-73 2018-09-10
*   Hotfixes, missing symlinks, libraries, dependencies, Ubuntu 18.04 compats, etc
*   ProgPOW ethminer updated


##### LINUX IMAGE RELEASE 0.5-73 2018-09-10
*   THIS IS BETA RELEASE
*   Upgraded to Ubuntu 18.04 LTS
*   Linux Kernel 4.15.0-33-generic
*   Nvidia driver 396.54 (with CUDA 9.2 support)
*   amdgpu-pro driver 18.20-606296


##### 0.5-72 2018-09-09
*   Reworked how agent runs gpu-stat, now it's a separate process. This should prevent rig to go offline with hanging AMD driver.
*   ProgPOW ethminer, 0.15 alpha cuda 9.2 (requires 396 driver)
*   Added CUDA 9.2 libs so ccminers can be recompiled now and used


##### ASIC 0.1-07 2018-09-07
*   Antminer E3
*   Antminer X3
*   Innosilicon A9
*   Teleconsole supported on ASICs
*   Hashrate watchdog
*   Fixed running shutdown from web
*   Fixed for some firmwares of Antminer D3 Blissz

   

##### 0.5-71 2018-09-07
*   `autofan` added reboot or shutdown action on reaching critical temp, minor improvements
*   Teleconsole client autoupdate
*   `disk-expand` utility to enlarge disk partition and use all the space on disk
*   ethminer - autodetect CUDA/OpenCL platforms
*   sgminer-gm - myriadcoin-groestl kernel +10%
*   `nvidia-oc` - added running delay option
*   Fixed "too many symbolic links levels" on WiFi installation
*   `amdmeminfo` updated
*   Fixed miner log for 3+ miner
*   cpuminer-opt cpu temp on AMD platform
*   custom miner will check it's name, prevent "file not found" errors
*   `nvidia-driver-update` will correctly install the latest 396 driver with CUDA 9.2 and nvidia-settings


##### 0.5-70 2018-08-24
*   `nvidia-driver-update` to update your Nvidia driver on old installations, currently 390.59 is the latest stable
*   Minor bugfixes


##### 0.5-69 2018-08-15
*   Minor bugfixes

 
##### 0.5-68 2018-08-11
*   Detecting GPU subvendor (msi, asus, ...)
*   Added OHGODAPILL_START_TIMEOUT in Nvidia OC for delayed pill starting, required for some 1080 not to crash
*   To get your external IP on the rig run `ip-external` 

##### 0.5-67 2018-08-06
*   ewbf 0.5
*   ccminer-enemy 1.14, use `ccminer-update`
*   t-rex-0.5.7 (as custom miner), use `custom-get http://download.hiveos.farm/custom/t-rex-0.5.7.tar.gz -f` to upgrade existing
*   xmrig-amd-2.7.3 xmrig-nvidia-2.7.0 released as custom miners, find them in http://download.hiveos.farm/custom
*   sgminer-avermore-1.4.1
*   `selfuprade` can accept version number for easier downgrade
*   `firstrun` will ask to change system password for SSH and VNC
*   `hive-passwd` new command to change system password

##### 0.5-66 2018-08-01
*   ewbf 0.4 fork added, though it's unstable
*   ethminer 0.15 stable release

##### 0.5-65 2018-07-22
*   xmr-stak 2.4.7
*   xmrig 2.6.4

##### 0.5-64 2018-07-13
*   Autofan will stop mining at 90°C by default to protect your GPU from burning.
    To reboot rig on driver error, fake temps like 511°C, fans malfunction you should enable `REBOOT_ON_ERROR=1` in `/hive-config/autofan.conf`.
    It's still manual option, web autofan config will be in Hive 2.0 very soon.
*   Easier choosing server mirror on the rig.
    Now you don't have to change it on web, you just run `firstrun -f` and set mirror you want.
    Server URL will be changed on the web if the connection succeeds.

##### 0.5-63 2018-07-11
*   Claymore Dual 11.9
*   cpuminer-opt accepted/rejected report, small bugfix
*   Autofan. Fixes for stability. New config option `REBOOT_ON_ERROR=1`, this will reboot rig if autofan can't read GPU temp or fan.
*   Small preparations for Hive 2.0 release


##### ASIC 0.1-06 2018-07-11
*   Antminer Z9-Mini support


##### 0.5-62 2018-07-04

*   NEW: Custom Miner Intergation support. [Forum page](http://forum.hiveos.farm/discussion/1273/custom-miner-integration).
*   tdxminer released as a custom miner package. Please find how to use it in wallet examples as "Custom tdxminer" (bottom of the wallets page).
*   ewbf 0.3 with equihash 96/5


##### 0.5-61 2018-06-29

*   Preparations for Hive 2.0 release
*   `PROJECT_HASH` is renamed to `FARM_HASH`
*   xmrig 2.6.3
*   autofans more improved



##### 0.5-60 2018-06-23
*   ewbf 0.2 fork with equihash 144/5, 192/7
*   autofans reworked and improved, still only manual config in /hive-config/autofan.conf



##### Windows 0.1-01 2018-06-20
*   Beta release of Hive for Windows



##### ASIC 0.1-05 2018-06-20
*   `PROJECT_HASH` support in config file


##### 0.5-59 2018-06-17
*   Autofans preview release, can be used with manual configuration in autofan.conf
*   Ccminer wildkeccak scratchpad will be removed if the pool is changed
*   cpuminer-opt 3.8.8.1


##### 0.5-58 2018-06-12
*   xmr-stak fireice-uk 2.4.5


##### 0.5-57 2018-06-07
*   bminer 8.0.0
*   `PROJECT_HASH` in rig.conf, new way of attaching your rigs to the account


##### 0.5-56 2018-06-05
*   Hotfix for AMD "Aggressive mode", claymore reboot, IGPU detection, ccminer start after reboot


##### 0.5-55 2018-06-04
*   New AMD undervolting is now optional. Please find "Aggressive mode" in AMD OC dialog.
*   xmr-stak fireice-uk 2.4.4
*   xmr-stak indeedminers 2.4.8
*   cpuminer-opt 3.8.8.1
*   ccminer-vertminer-1.0.3
*   claymore 11.8
*   SRRv2 Extension Board support


##### ASIC 0.1-04 2018-06-03
*   Antminer S9i
*   Antminer L3++
*   Antminer D3 Blissz


##### 0.5-54 2018-06-01
*   IMPORTANT! New AMD undervolting technique, more reliable core voltage states now. Though it's slower to apply.
*   Invalid shares reported by Claymore for each GPU


##### LINUX IMAGE RELEASE 0.5-53 2018-05-24
*   Fixed NTFS config partition mounting at boot
*   Nvidia 390.59 driver


##### 0.5-53 2018-05-24
*   Accepted / Rejected shares stats for most of the miners
*   Added selection xmr-stak forks FireiceUK or IndeedMiners
*   Removed obsolete xmr-stak-cpu
*   Reworked NTFS config partition mounting
*   Improved online detection at boot


##### 0.5-52 2018-05-19

*   Added "Disable GUI on boot (don't start X server, console only, no OC for Nvidia)" in Tuning dialog
*   dstm reverted from 0.6.1 to 0.6.0, too many complaints
*   ethminer 0.14.0 stable
*   ethminer 0.15.dev10
*   sgminer avermore 1.4
*   xmr-stak 2.4.7 IndeedMiners

##### 0.5-51 2018-05-14

*   dstm 0.6.1
*   xmrig 2.6.2
*   AMD Ryzen temperatures (k10temp kernel module), use `hive/opt/k10temp/install.sh` to install driver
*   Added support for more China Dogs (device ids 5131:2007, 0471:2379)
*   Added CUDA 9.1 libs to ccminer if you have custom builds and want to run them


##### ASIC 0.1-03 2018-05-12

*   Antminer T9+
*   Added config override on the web so you can set "bitmain-freq", "bitmain-fan-ctrl" and other settings

##### 0.5-50 2018-05-05

*   bminer 7.0.0
*   ethminer 0.14.0rc4->rc9, 0.15.0dev4->dev7
*   sgminer-avermore (x16r) ver. 1.3
*   lolMiner-mnx 0.3.4
*   Fixed P102-100 overclocking
*   Added OhGodAnETHlargementPill commandline arguments in OC dialog on the web so you can set `--revA` for old 1080s
*   Fixed `gpu-fans-find` timeouts
*   Bios download will include rig name in filename


##### 0.5-49 2018-05-02

*   After lot's of reports about OhGodAnETHlargementPill is not enabled by default. You can enable it in Nvidia OC dialog now.


##### 0.5-48 2018-04-30

*   OhGodAnETHlargementPill in the box, gives up to 52Mh on 1080ti (https://github.com/OhGodACompany/OhGodAnETHlargementPill)
*   Claymore Dual 11.7
*   cpuminer-opt 3.8.8

##### 0.5-47 2018-04-20

*   Fixed Chinese Watchdogs, they were detected but did not really work
*   Fixed xmr-stak parsing that showed GPU temps
*   Fixed ethminer wallet config from nanopool and others whicah had slahes in template, like %EWAL/%WORKER_NAME%
*   ccminer-enemy 1.08 (z-enemy) available for update by running ccminer-update

##### 0.5-46 2018-04-20

*   xmr-stack 2.4.3
*   xmrig 2.6.0 beta3
*   ethminer 0.15 dev3
*   sgminer avermore replaced x16r fork
*   NEW: SimpleRigResetter SSRv2 Watchdog support, [usage instructions on forum](http://forum.hiveos.farm/discussion/694/simplerigresetter-ssrv2-watchdog)

##### LINUX IMAGE RELEASE 0.5-45 2018-04-19

*   Logs are OFF by default
*   Linux 4.13 kernel
*   Installed ROCm with AMD driver to support Vega
*   Configs partition is now NTFS
*   Intel's E1000E updated network driver by default

##### 0.5-45 2018-04-17

*   NEW: cpuminer-opt
*   ethminer 0.14 and 0.15 in the box, version can be selected in the wallet
*   amdmeminfo updated

##### 0.5-44 2018-04-13

*   [Teleconsole](https://www.teleconsole.com/). You can access your rig's console from anywhere without VPN or local network access. Run `telec start` from the web and then join the session from browser or local console. [Forum thread](http://forum.hiveos.farm/discussion/649/teleconsole).
*   ethminer 0.15-dev1. Note, there are slight config syntax changes. So for Nicehash you need stratum2+tcp:// protocol in the wallet. Refer to miner's help.
*   ccminer-enemy 1.0.5 available, run ccminer-update to replace existing version


##### 0.5-43 2018-04-10

*   sgminer-gm 5.5.6, cryptonight v7 support, set `"monero": "true"` in wallet config

##### 0.5-42 2018-04-09

*   lolminer 0.33
*   xmrig v2.6.0-beta2
*   Fixed CPUs count for xmr-stak

##### ASIC 0.1-02 2018-04-09

*   Antminer D3
*   Antminer A3
*   Antminer L3+
*   Fixed issues on S9


##### 0.5-41 2018-04-05

*   ccminer-klaust-8.21
*   ccminer-nevermore-0.2.2
*   ccminer-rvn-2.3
*   Claymore CryptoNote 11.3
*   xmrig fixed IPv6 issue
*   xmr-stak 2.4.2
*   wifi script will detect "ra0" interfaces instead on "wlan0" for Ralink


##### 0.5-40 2018-04-04

*   NEW: sgminer-x16r 0.4.0 (supports x16s also), replaced [aceneun](https://github.com/aceneun/sgminer-gm-x16r/tree/x16r) fork with [brian112358](https://github.com/brian112358/sgminer-x16r/releases) fork
*   Claymore 11.6
*   xmrig 2.5.2
*   xmrstack 2.4.0
*   ccminer suprminer 1.5, tprvot 2.2.5, run `ccminer-update` to get newer version
*   Improved stats availability on rigs with high system load, recent ccminer could cause that with 8+ GPUs
*   Intel E1000E network driver update script. Run `/hive/opt/e1000e/e1000e-upgrade.sh` to update your current driver. Possibly can fix issues with hanging subnetworks.


##### 0.5-39 2018-03-26

*   Fixed optiminer-install "no space" error
*   firstrun now allows to set server URL for first connection, this is useful when default server URL does not work


##### 0.5-38 2018-03-24

*   NEW: optiminer. This miner is very heavy and is not included in the package. To use it you should run optiminer-install on the rig via SSH or Linux Shell from the web (it will take time to download).
*   Added support for Chinese Watchdogs (QinHeng Electronics HL-340). Those that have orange blocks, you saw them on Ali and Ebay.
*   "Dude, where is my GPU?". `gpu-fans-find` script to find GPU by spinning fans


##### 0.5-36 2018-03-18

*   NEW: lolMiner 0.31 (for equihash 96/5, MNX coin)
*   Claymore Dual 11.5, removed 11.1
*   ethminer 0.14.0-dev4
*   /home/user/xinit.user.sh user script to by run in terminal after start. You could put there `tail -f /run/hive/miner.1` to see miner output after graphical interface (X server) starts.


##### 0.5-35 2018-03-13

*   Claymore Dual 11.4, removed 11.3

##### 0.5-34 2018-03-12

*   Claymore Dual 11.3

##### 0.5-33 2018-03-10

*   Claymore Dual 11.2
*   bminer 5.5.0
*   OpenVPN now supports login and pass (auth-user-pass config option)
*   Added "sibcoin" algo to selection of sgminer
*   sgminer x16r

##### LINUX IMAGE RELEASE 0.5-32 2018-01-28

*   Nvidia driver 390.25
*   AMDGPU-PRO driver 17.50
*   memtest86+
*   Intel CPU microcodes

##### 0.5-32 2018-02-28

*   nForce IGPU fix
*   Calymore Dual 11.1

##### 0.5-31 2018-02-26

*   dstm 0.6.0, supports failover pools now
    
    !!! config syntax had changed, you need to check your wallets !!!
    
*   bminer 0.5.4
*   Hive will deliver 3 latest versions of Claymore Dual Miner. It can be selected in a wallet. Currently it's 11.0, 10.6, 10.5.
*   `net-test` shell command to test network connection to Hive servers
*   NEW: ccminer allium (Garlicoin)

##### 0.5-30 2018-02-11

*   Logs totally reworked. All miner logs are now in /var/log/miner/*
*   Logs can be putted in RAM now, USB flash drive owners will love this. Run `logs-off` to remount /var/log to tmpfs, reboot required. Run `logs-on` to remount /var/log to disk, reboot required.
*   GPU Power draw reporting, find it on the rigs page. Don't trust it too much, this is just a driver info.
*   FIX: sgminer gm-nicehash fork was broken
*   FIX: ccminer didn't show hashes on driver fail

##### 0.5-29 2018-02-08

*   Fixed temp stats for xmr-stak with GPUs enabled
*   Fixed amd-info sorting order by bus id on some old motherboards (Asus P5QL-E)
*   bminer 5.3.0
*   Claymore Dual 11.0 +blake2s +keccak
*   NEW ccminer-rvn for x16r

##### 0.5-XX 2018-01-28

*   Fixed bminer hashes order in stats for 10+ gpus systems

##### 0.5-26 2018-02-02

*   Timezone on the rig will be applied from your account timezone
*   NEW sgminer djm34 for Lyra2Z and Lyra2H
*   Added cron job to restart agent if it's not running, as this was reported on some systems

##### 0.5-24 2018-01-31

*   FIXED ccminer-phi-anxmod recompiled with CUDA8, now working. Run "ccminer-update" to redownload it.
*   NEW ccminer-dace-cryptonight
*   other small fixes

##### 0.5-23 2018-01-30

*   NEW Bminer
*   NEW xmr-stak AMD Nvidia CPU
*   NEW xmrig CPU

##### 0.5-22 2018-01-28

*   Updated amdmeminfo, more accurate mem type detection
*   Claymore Dual 10.6
*   Claymore CryptoNote 11.2
*   Ethminer 0.13
*   NEW ccminer-alexis-1.5.3
*   NEW ccminer-bcd-1.0.0
*   NEW ccminer-djm34-0.3.0
*   NEW ccminer-klaust-8.19
*   NEW ccminer-nanashi-2.2.mod.r2
*   NEW ccminer-phi-anxmod-1.0
*   NEW ccminer-sp-mod-1.5.81
*   NEW ccminer-tpruvot-2.2.4
*   NEW ccminer-xevan-0.1
*   Ccminers are now auto downloaded if used, no need for manual installation anymore
*   NEW sgminer-gatelessgate 0.1.3-pre6b, Neosrypt for AMD cards
*   NEW sgminer-phi 5.6.1, Phi for AMD cards
*   Sgminer and Ccminer now support failover pools from the wallet

##### 0.5-20 2018-01-24

*   P106-090 support added
*   Claymore Dual 10.5
*   ccminer-tpruvot 2.2.4
*   Other small changes and fixes

##### 0.5-19 2018-01-09

*   "Overclocking Profile" required changes so that is can be applied from the web. This is a required update if you want to use this feature.
*   Tweaked filesystem mount options in /etc/fstab so that USB flash drives will work longer (noatime,commit=120)
*   Much quicker Nvidia OC applying on the rig

##### 0.5-18 2018-01-03

*   Nvidia P104-100 support
*   dstm 0.5.8

##### 0.5-17 2017-12-28

*   Added "vm.nr_hugepages=128" and "* hard memlock 262144" "* soft memlock 262144" to fix "MEMORY ALLOC FAILED: mlock failed" in xmr-stack-cpu
*   OpenDev Watchdogs ids updated for new Pro devices, added "0483:a26d"
*   Esonics Watchdogs support added
*   Added "--report-hashrate" as a default ethminer option in config
*   Minor fixes with GPU order after restart. False "Selfupgrade successful" message on fail.

##### 0.5-16 2017-12-25

*   Miner start problem after reboot seems to be resolved. The issue is related to slow flash drives.
*   xorg.conf for Nvidia is generated more wisely now. If you had GPUs with pci ids like 3c:00:0. 8b:00:0 (etc.) this will help you.
*   ccminer Gh/s bug fix improved. Some GPUs do not have idle load at 0%, but 3-4% of load. Now this is also detected.

##### 0.5-14 2017-12-22

*   dstm 0.5.7
*   Claymore CryptoNote 11.0
*   ccminer Gh/s bug prevented. Ccminer fails and begin to report giga hashes though it's not mining. Now hive agent inspects GPU load % and if it's 0 then it does not believe ccminer anymore and sets hashrate to 0.
*   WiFi online status is checked with other service now, so no more delays at startup. Also that could cause not working WiFi after reboot, please check again if you had problems before. And this relates to systems with multiple network interfaces.
*   Added AMD OC Mem State selection, some GPUs found to require this to undervolt
*   AMD bios downloads have pretty names now like "vbios-0-RadeonRX470-4G--113-1E3471U_O69.rom"
*   Added force option to AMD bios flashing
*   OpenVPN now will accept client.conf with embedded certificates in one file
*   Removed "127.0.0.1 cryptonight.usa.nicehash.com" from /etc/hosts as Nicehash is back again
*   WatchdogInUa updated binary to support PWR command

##### 0.5-12 2017-12-11

*   AMD undervolting now works from panel! Please set core voltage like 900 with DMP desired level.
*   Added `127.0.0.1 cryptonight.usa.nicehash.com` and `127.0.0.1 daggerhashimoto.usa.nicehash.com` to /etc/hosts because Claymore DevFee could not miner there and crashed
*   ccminer recompiled for event more CPU platforms like old AMD Phenom II
*   ccminer could show hashrate even when GPU was hang, now stats detect this by zero temp on that card
*   `amd-info` more convenient way to show AMD clocks
*   `rocm-smi` more another utility for AMD clocks
*   Turn Off LEDs on Nvidias from OC dialog. May not work on some cards.
*   Latest drivers amdgpu-pro-17.40-492261 and NVIDIA-Linux-x86_64-387.34. DOES NOT AUTOUPDATE, ONLY WITH NEW IMAGE
*   Custom compiled Linux Kernel. DOES NOT AUTOUPDATE, ONLY WITH NEW IMAGE
*   Claymore reboot did not actually happen on hang, fixed

##### 0.5-10 2017-12-06

*   ccminer 2.2.3. Compiled to support more platforms including AMD CPUs, added "phi" algo for LUX coin and others. Requires driver 384+ so you will need to upgrade very old systems if you want it.

##### 0.5-09 2017-12-05

*   Rolling back to Claymore Dual 10.1, as the 10.2 has many complaints
*   On some systems miner started before Nvidia OC applied
*   Claymore will send part of it's last log on reboot

##### 0.5-08 2017-12-02

*   dstm 0.5.6
*   Claymore Dual 10.2
*   Fixed stats for R9 295x2
*   Claymore Dual config generation fixed again, setting "-mode 1" for solo mode and removing "-dcri" and "-dcoin" arguments
*   "Rig Boot" event option in Telegram Notifications

##### 0.5-06 2017-11-08

*   Claymore CryptoNote
*   Miners now report active algorithm
*   Nvidia OC settings did not apply to 13th card
*   Fixed setting "-dcri 0" in claymore config if no DPOOL set
*   Added big Nicehash wallet example
*   Other minor fixes

##### 0.5-05 2017-11-05

*   dstm 0.5.4, gpu ordering fixes, fixed hashrate report on pool disconnect (?)
*   AMD OC applied in wrong order for 10+ cards
*   Reboot and Shutdown commands improved
*   Readonly claymore's management port, so no more hacking

##### 0.5-04 2017-10-30

*   Fixed Claymore reboot, agent was killed and rig went offline, reboot did not happen
*   Fixed Nvidia GPU order right after reboot
*   Log truncate did not work
*   Claymore config generator will set DCRI to 0 if no DCOIN set, this will add some Mh on AMD cards

##### 0.5-03 2017-10-29

*   Claymore 10.1, dstm 0.5.3
*   Fixed bug with non starting miner, overwriting config update upgrade
*   Added EWBF custom settings field
*   Changed behavior on naming rigs. If you had rig named with only numbers like "1", then the WORKER_NAME was prefixed with "hive1". It was confusing so this is not true anymore, it will stay "1".

##### LINUX IMAGE RELEASE 0.5-01 2017-10-27

*   Second miner. You can launch 2 miners at the same time. Maybe you will want CPU miner or separate miners for AMD and Nvidia cards.
*   New miners: ethminer, sgminer-gm, dstm, xmr-stak-cpu.
*   AMD driver 17.40 with DAG fix, OC+downvolt still do not work together. ROCm kernel removed to save space.
*   Nvidia GPU order is now the same as PCI bus id, so order in miner and rig admin is the same now, much easier to overclock
*   Internal GPU detection, now you can use monitor on internal GPU with Nvidias
*   miner will start only after Nvidia OC will be applied
*   miners rotates 5 logs now between restarts so you can examine previous runs
*   Trying to handle nvidia-smi hangs, maybe a reason for agent stop
*   Hive FAT partition will be visible in Windows, some versions had problems
*   Static IP and WiFI config files can be edited from Windows now
*   `sreboot shutdown` – more aggressive shutdown command
*   `watchdog-opendev reset|power` – to send command to OpenDev watchdogs
*   `miner log` with color as it is on a real screen now seen on the web

##### LINUX IMAGE RELEASE 0.4-20 2017-10-14

*   ccminer 2.2.2 (CUDA 7.5), supports 10+ cards
*   Nvidia default power limit is restored after setting back to 0 in OC settings
*   /hive-config/http_proxy.txt to set HTTP PROXY, you can edit file from Windows

##### 0.4-17 2017-10-12

*   Hashrate Watchdog. You can set minimal hashrate for each miner in "Tuning". If it drops below minimal then there will be attempt to restart miner. If miner restart does not help, then reboot will be done.
*   ewbf "API bind error" solved, no more "Miner Offline" after restart


##### LINUX IMAGE RELEASE 0.4-13 2017-10-07

*   DAG fix for AMD. New image has dual boot now, kernel 4.10 by default (without fix) and ROCm patched kernel 4.11 (with DAG fix). The down side of fix is that when you set Core or Mem clock then downvolting will NOT work. Though you can flash VBIOS with proper frequencies and set DPM downvolting states from the web.
*   Downgraded AMD drivers to 16.60 for DPM (downvolting) to work.
*   Changed AMD OC power management. Removed Voltage Index and added DPM Core States for downvolting.
*   Added "Tuning" button in rig profile. Now you can override any individual setting from the wallet.
*   Added miner "restart", "last log" and "show config" buttons
*   Motherboard model and kernel version in the rig profile now
*   WiFi setup script, just run `wifi` to try
*   Force reboot script, helps a lot with hanging GPUs where standard reboot does not work, run `sreboot` to try
*   Fixed GPU stats order for mixed setups
*   /hive-config is now on FAT partition, you can set ID and pass from your ugly Windows)
*   VNC password is stored in /hive-config/vnc-password.txt now. And you can disable VNC.
*   Added `pci=noaer iommu=soft` options to grub bootloader, no more flooding errors on the screen. IOMMU motherboards (like GA-970A-DS3P) will work from the box.


##### 0.4-01 2017-09-29

*   ccminer 2.2.1
*   OC and upgrade do not block agent anymore, rig stays alive, panic no more
*   WEB: lots of refactoring, wallets visual improvements

##### LINUX IMAGE RELEASE 0.3-55 2017-09-20

*   Claymore Dual Miner 10.0
*   IMG: Fixed duplicate IP address on MikroTik routers, now ClientId is strictly MAC address
*   IMG: Added support for Killer Network NIC (MSI Gaming M3 motherboard)
*   IMG: Nvidia 970 tested, driver loads, but no OC available
*   IMG: Updated Nvidia driver to 384.69
*   Agents traffic is now in /var/log/hive-agent.log, reboot required
*   Fixed hourly log rotation, it was daily and some system ran out of space with lots of kernel error messages
*   REBOOT RECOMMENDED

##### 0.3-47 2017-08-21

*   Added support for Nvidia P106-100 GPUs, tested 13 cards on one board
*   Added support for OpenDev Watchdogs
*   Fixed bug with not starting agent after reboot
*   WEB: added more example wallets with templates



##### 0.3-42 2017-08-09

*   Fixed connected detection for Nvidia
*   connect-timeout increased from 2 to 7 seconds, this helps on high latency network
*   Claymore Dual 9.8
*   Claymore Zcash 12.6
*   Added caching hive host DNS resolve in /etc/hosts
*   WEB: added transfer rig to another account button

  

##### 0.3-37 2017-08-06

*   Console service which starts if X server is failing so you can use shell on tty1
*   Fixed 8th AMD card temp and fans stats on some setups
*   Improved internal GPU detection
*   WEB: Multiple rigs selection and applying miner, wallet (and other actions) to selected rigs
*   WEB: Added "Create example wallet for nanopool" link
*   WEB: Added "Copy" function action to the wallet

  

##### 0.3-33 2017-08-02

*   Added Claymore ZCash AMD miner
*   Changing wallet will apply it to the rig automatically
*   Now you can override settings in config.txt for Claymore (look in wallet settings for it)
*   Tested on the rig with 13 Nvidia GPUs, changed xorg.conf a bit

  

##### 0.3-25 2017-07-30

*   AMD overclocking
*   AMD VBIOS ROM download
*   AMD VBIOS ROM flashing
*   Extended info about GPUs, available RAM, memory type for AMD, max pow limit for NVIDIA
*   Rigs remote IP address detection

  

##### 0.3-23 2017-07-26

*   OpenVPN config and keys upload
