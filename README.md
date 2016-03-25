# munin-patch

for munin-2.0.25 on CentOS 7 (munin-2.0.25-2.el7.noarch)

- LimitsOld.pm
    - ときどき OKs だけの通知が送られる問題を修正
    - `/var/lib/munin/limits.storable` が欠損することが原因？
    - 根本の原因は munin-update の UpdateWorker が中途半端に実行されているため？
    - 原因不明だけど、state が空から ok に遷移するときは通知しないように変更
