---
layout: post
title:  "Benchmarking Uguu 1.8.4 & 1.8.5"
---

## Uguu 1.8.4
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

## Uguu 1.8.5
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

## Conclusion
Changing to PHP's new built-in randomizer (available in PHP 8.3), nets a small gain. As the database fills upp with records the performance gets worse however. Some database tuning and keeping an index of some rows would probably improve performance as the database fills up.