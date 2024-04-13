---
layout: post
title:  "Benchmarking Uguu 1.8.4 & 1.8.5"
---

## Uguu 1.8.4 (with file-copy & without index)
```
Uguu V1.8.4 using SQLite.
MacBook Pro M1 2020, 16GB RAM, 256GB SOC-STORAGE, Sonoma 14.4.1.
Test file size: 1.97MB.
PHPBench (1.2.15) running benchmarks...
with PHP version 8.3.6, xdebug ❌, opcache ❌

\Pomf\Uguu\Benchmarks\UguuBench

    benchTest...............................I14 - Mo2.223ms (±9.69%)

Subjects: 1, Assertions: 0, Failures: 0, Errors: 0
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| iter | benchmark | subject   | set | revs | mem_peak   | time_avg    | comp_z_value | comp_deviation |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| 0    | UguuBench | benchTest |     | 500  | 7,027,568b | 1,828.430μs | -1.87σ       | -18.14%        |
| 1    | UguuBench | benchTest |     | 500  | 7,027,568b | 1,955.430μs | -1.29σ       | -12.45%        |
| 2    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,073.294μs | -0.74σ       | -7.18%         |
| 3    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,068.880μs | -0.76σ       | -7.37%         |
| 4    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,115.536μs | -0.55σ       | -5.29%         |
| 5    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,641.094μs | +1.88σ       | +18.24%        |
| 6    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,339.276μs | +0.49σ       | +4.73%         |
| 7    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,213.622μs | -0.09σ       | -0.89%         |
| 8    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,174.556μs | -0.27σ       | -2.64%         |
| 9    | UguuBench | benchTest |     | 500  | 7,027,568b | 2,241.680μs | +0.04σ       | +0.36%         |
| 10   | UguuBench | benchTest |     | 500  | 7,027,568b | 2,672.708μs | +2.03σ       | +19.66%        |
| 11   | UguuBench | benchTest |     | 500  | 7,027,568b | 2,235.492μs | +0.01σ       | +0.09%         |
| 12   | UguuBench | benchTest |     | 500  | 7,027,568b | 2,306.292μs | +0.34σ       | +3.26%         |
| 13   | UguuBench | benchTest |     | 500  | 7,027,568b | 2,300.502μs | +0.31σ       | +3.00%         |
| 14   | UguuBench | benchTest |     | 500  | 7,027,568b | 2,337.002μs | +0.48σ       | +4.63%         |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
```

## Uguu 1.8.4 (without file-copy & with index)
```
Uguu V1.8.4 using SQLite.
MacBook Pro M1 2020, 16GB RAM, 256GB SOC-STORAGE, Sonoma 14.4.1.
Test file size: 1.97MB.
PHPBench (1.2.15) running benchmarks...
with PHP version 8.3.6, xdebug ❌, opcache ❌

\Pomf\Uguu\Benchmarks\UguuBench

    benchTest...............................I14 - Mo1.057ms (±2.08%)

Subjects: 1, Assertions: 0, Failures: 0, Errors: 0
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| iter | benchmark | subject   | set | revs | mem_peak   | time_avg    | comp_z_value | comp_deviation |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| 0    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,134.830μs | +3.15σ       | +6.54%         |
| 1    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,066.098μs | +0.04σ       | +0.09%         |
| 2    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,058.688μs | -0.29σ       | -0.61%         |
| 3    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,052.888μs | -0.55σ       | -1.15%         |
| 4    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,058.072μs | -0.32σ       | -0.66%         |
| 5    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,052.422μs | -0.57σ       | -1.19%         |
| 6    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,063.364μs | -0.08σ       | -0.17%         |
| 7    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,053.182μs | -0.54σ       | -1.12%         |
| 8    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,054.152μs | -0.50σ       | -1.03%         |
| 9    | UguuBench | benchTest |     | 500  | 6,769,784b | 1,060.954μs | -0.19σ       | -0.39%         |
| 10   | UguuBench | benchTest |     | 500  | 6,769,784b | 1,055.328μs | -0.44σ       | -0.92%         |
| 11   | UguuBench | benchTest |     | 500  | 6,769,784b | 1,054.990μs | -0.46σ       | -0.95%         |
| 12   | UguuBench | benchTest |     | 500  | 6,769,784b | 1,102.530μs | +1.69σ       | +3.51%         |
| 13   | UguuBench | benchTest |     | 500  | 6,769,784b | 1,052.966μs | -0.55σ       | -1.14%         |
| 14   | UguuBench | benchTest |     | 500  | 6,769,784b | 1,056.776μs | -0.38σ       | -0.79%         |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
```

## Uguu 1.8.5 (with file-copy & without index)
```
Uguu V1.8.5 using SQLite.
MacBook Pro M1 2020, 16GB RAM, 256GB SOC-STORAGE, Sonoma 14.4.1.
Test file size: 1.97MB.
PHPBench (1.2.15) running benchmarks...
with PHP version 8.3.6, xdebug ❌, opcache ❌

\Pomf\Uguu\Benchmarks\UguuBench

    benchTest...............................I14 - Mo2.035ms (±9.47%)

Subjects: 1, Assertions: 0, Failures: 0, Errors: 0
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| iter | benchmark | subject   | set | revs | mem_peak   | time_avg    | comp_z_value | comp_deviation |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| 0    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,736.310μs | -1.63σ       | -15.41%        |
| 1    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,775.586μs | -1.43σ       | -13.50%        |
| 2    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,821.816μs | -1.19σ       | -11.25%        |
| 3    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,857.194μs | -1.01σ       | -9.52%         |
| 4    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,950.312μs | -0.53σ       | -4.99%         |
| 5    | UguuBench | benchTest |     | 500  | 7,026,656b | 2,046.102μs | -0.03σ       | -0.32%         |
| 6    | UguuBench | benchTest |     | 500  | 7,026,656b | 2,101.118μs | +0.25σ       | +2.36%         |
| 7    | UguuBench | benchTest |     | 500  | 7,026,656b | 1,964.758μs | -0.45σ       | -4.28%         |
| 8    | UguuBench | benchTest |     | 500  | 7,026,656b | 2,004.724μs | -0.25σ       | -2.34%         |
| 9    | UguuBench | benchTest |     | 500  | 7,026,656b | 2,129.382μs | +0.39σ       | +3.74%         |
| 10   | UguuBench | benchTest |     | 500  | 7,026,656b | 2,232.738μs | +0.93σ       | +8.77%         |
| 11   | UguuBench | benchTest |     | 500  | 7,026,656b | 2,226.850μs | +0.90σ       | +8.48%         |
| 12   | UguuBench | benchTest |     | 500  | 7,026,656b | 2,287.736μs | +1.21σ       | +11.45%        |
| 13   | UguuBench | benchTest |     | 500  | 7,026,656b | 2,342.434μs | +1.49σ       | +14.11%        |
| 14   | UguuBench | benchTest |     | 500  | 7,026,656b | 2,313.586μs | +1.34σ       | +12.71%        |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
```

## Uguu V1.8.5 (without file-copy & with index)
```
Uguu V1.8.5 using SQLite.
MacBook Pro M1 2020, 16GB RAM, 256GB SOC-STORAGE, Sonoma 14.4.1.
Test file size: 1.97MB.
PHPBench (1.2.15) running benchmarks...
with PHP version 8.3.6, xdebug ❌, opcache ❌

\Pomf\Uguu\Benchmarks\UguuBench

    benchTest...............................I14 - Mo1.057ms (±2.21%)

Subjects: 1, Assertions: 0, Failures: 0, Errors: 0
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| iter | benchmark | subject   | set | revs | mem_peak   | time_avg    | comp_z_value | comp_deviation |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
| 0    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,057.302μs | -0.72σ       | -1.59%         |
| 1    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,053.900μs | -0.86σ       | -1.90%         |
| 2    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,051.952μs | -0.94σ       | -2.08%         |
| 3    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,062.180μs | -0.51σ       | -1.13%         |
| 4    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,116.234μs | +1.76σ       | +3.90%         |
| 5    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,094.810μs | +0.86σ       | +1.90%         |
| 6    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,104.362μs | +1.26σ       | +2.79%         |
| 7    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,110.690μs | +1.53σ       | +3.38%         |
| 8    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,105.174μs | +1.30σ       | +2.87%         |
| 9    | UguuBench | benchTest |     | 500  | 6,768,872b | 1,079.362μs | +0.21σ       | +0.47%         |
| 10   | UguuBench | benchTest |     | 500  | 6,768,872b | 1,056.294μs | -0.76σ       | -1.68%         |
| 11   | UguuBench | benchTest |     | 500  | 6,768,872b | 1,056.178μs | -0.77σ       | -1.69%         |
| 12   | UguuBench | benchTest |     | 500  | 6,768,872b | 1,056.820μs | -0.74σ       | -1.63%         |
| 13   | UguuBench | benchTest |     | 500  | 6,768,872b | 1,058.032μs | -0.69σ       | -1.52%         |
| 14   | UguuBench | benchTest |     | 500  | 6,768,872b | 1,051.938μs | -0.94σ       | -2.09%         |
+------+-----------+-----------+-----+------+------------+-------------+--------------+----------------+
```