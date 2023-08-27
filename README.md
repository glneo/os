<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 5:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-08-27&nbsp;02:28:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-27&nbsp;02:28:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-08-27&nbsp;02:28:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-08-27&nbsp;02:28:38</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-08-27&nbsp;02:28:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-08-27&nbsp;02:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-08-27&nbsp;02:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-08-27&nbsp;02:28:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R6S</a></td><td align="left">2023-08-27&nbsp;02:28:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R6S</a></td><td align="left">2023-08-27&nbsp;02:28:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-08-27&nbsp;02:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-08-27&nbsp;02:28:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-08-27&nbsp;02:28:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-08-27&nbsp;02:28:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:46</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:47</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-08-27&nbsp;02:28:47</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-27&nbsp;02:28:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-08-27&nbsp;02:28:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-08-27&nbsp;02:28:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-08-27&nbsp;02:28:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-08-27&nbsp;02:28:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-08-27&nbsp;02:28:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-08-27&nbsp;02:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-08-27&nbsp;02:28:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-08-27&nbsp;02:28:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-08-27&nbsp;02:28:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-08-27&nbsp;02:28:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-08-27&nbsp;02:28:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-08-27&nbsp;02:28:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-08-27&nbsp;02:28:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ODROID M1</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ODROID M1</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-08-27&nbsp;02:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-08-27&nbsp;02:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-08-27&nbsp;02:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-08-27&nbsp;02:28:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-27&nbsp;02:28:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-27&nbsp;02:28:13</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-27&nbsp;02:28:14</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-27&nbsp;02:28:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-08-27&nbsp;02:28:14</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-08-27&nbsp;02:28:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-08-27&nbsp;02:28:16</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-08-27&nbsp;02:28:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-27&nbsp;02:28:51</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-27&nbsp;02:28:51</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-27&nbsp;02:28:52</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-27&nbsp;02:28:52</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-27&nbsp;02:28:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-27&nbsp;02:28:16</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eboleqozon">Orange Pi 5 Plus</a></td><td align="left">2023-08-27&nbsp;02:31:28</td><td align=right>5.10.160-rk35xx</td><td align=right>890</td><td align=right>15853</td></tr><tr><td align="left"><a href="https://paste.armbian.com/odemavoxef">Orange Pi 5 Plus</a></td><td align="left">2023-08-27&nbsp;02:34:07</td><td align=right>5.10.160-rk35xx</td><td align=right>890</td><td align=right>15493</td></tr><tr><td align="left"><a href="https://paste.armbian.com/odemavoxef">Orange Pi 5 Plus</a></td><td align="left">2023-08-27&nbsp;02:34:20</td><td align=right>5.10.160-rk35xx</td><td align=right>890</td><td align=right>15493</td></tr><tr><td align="left"><a href="https://paste.armbian.com/odemavoxef">Orange Pi 5 Plus</a></td><td align="left">2023-08-27&nbsp;02:34:22</td><td align=right>5.10.160-rk35xx</td><td align=right>890</td><td align=right>15493</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-08-27&nbsp;02:28:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-08-27&nbsp;02:28:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-08-27&nbsp;02:28:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/cicanuqoqi">NanoPi R1</a></td><td align="left">2023-08-27&nbsp;02:41:49</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>90</td><td align=right>2762</td></tr><tr><td align="left"><a href="https://paste.armbian.com/etorayepeq">Khadas VIM3</a></td><td align="left">2023-08-27&nbsp;02:32:37</td><td align=right>6.1.48-current-meson64</td><td align=right>890</td><td align=right>7773</td></tr><tr><td align="left"><a href="https://paste.armbian.com/mahiqamoco">Khadas VIM3</a></td><td align="left">2023-08-27&nbsp;02:36:55</td><td align=right>6.1.11-meson64</td><td align=right>908</td><td align=right>7517</td></tr><tr><td align="left"><a href="https://paste.armbian.com/pukeganose">Khadas VIM3</a></td><td align="left">2023-08-27&nbsp;02:41:11</td><td align=right>6.4.12-edge-meson64</td><td align=right>890</td><td align=right>7258</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sejolonibe">Khadas VIM3</a></td><td align="left">2023-08-27&nbsp;02:45:32</td><td align=right>6.2.0-rc3-meson64</td><td align=right>890</td><td align=right>7276</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-08-27&nbsp;02:28:23</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-08-27&nbsp;02:28:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-08-27&nbsp;02:28:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-08-27&nbsp;02:28:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-08-27&nbsp;02:28:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-27&nbsp;02:28:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-08-27&nbsp;02:28:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-08-27&nbsp;02:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-08-27&nbsp;02:28:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-27&nbsp;02:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-27&nbsp;02:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-27&nbsp;02:28:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-27&nbsp;02:28:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-27&nbsp;02:28:23</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-27&nbsp;02:28:23</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-27&nbsp;02:28:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-27&nbsp;02:28:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
