# k6 load tests

# Время 60 с, количество потоков 1, количество соединений 1, No Cache (MariaDB)

data_received..................: 783 kB 13 kB/s
data_sent......................: 244 kB 4.1 kB/s
http_req_blocked...............: avg=6.05µs  min=2µs    med=5µs     max=2.3ms p(90)=7µs     p(95)=8µs
http_req_connecting............: avg=85ns    min=0s     med=0s      max=224µs p(90)=0s      p(95)=0s
http_req_duration..............: avg=22.71ms min=5.95ms med=20.59ms max=1.06s p(90)=31.47ms p(95)=37.41ms
{ expected_response:true }...: avg=22.71ms min=5.95ms med=20.59ms max=1.06s p(90)=31.47ms p(95)=37.41ms
http_req_failed................: 0.00%  ✓ 0         ✗ 2622
http_req_receiving.............: avg=92.86µs min=45µs   med=86µs    max=577µs p(90)=120µs   p(95)=139.94µs
http_req_sending...............: avg=27.21µs min=12µs   med=24µs    max=419µs p(90)=36µs    p(95)=43µs
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s      max=0s    p(90)=0s      p(95)=0s
http_req_waiting...............: avg=22.59ms min=5.83ms med=20.48ms max=1.06s p(90)=31.34ms p(95)=37.3ms
http_reqs......................: 2622   43.615325/s
iteration_duration.............: avg=22.9ms  min=6.24ms med=20.78ms max=1.06s p(90)=31.66ms p(95)=37.64ms
iterations.....................: 2622   43.615325/s
vus............................: 1      min=1       max=1
vus_max........................: 1      min=1       max=1

# Время 60 с, количество потоков 1, количество соединений 1, Use Cache (MariaDB)

data_received..................: 576 kB 9.6 kB/s
data_sent......................: 179 kB 3.0 kB/s
http_req_blocked...............: avg=5.86µs  min=2µs    med=5µs     max=1.44ms p(90)=7µs     p(95)=8µs
http_req_connecting............: avg=118ns   min=0s     med=0s      max=228µs  p(90)=0s      p(95)=0s
http_req_duration..............: avg=30.87ms min=4.63ms med=23.4ms  max=3.03s  p(90)=41.62ms p(95)=56.91ms
{ expected_response:true }...: avg=30.87ms min=4.63ms med=23.4ms  max=3.03s  p(90)=41.62ms p(95)=56.91ms
http_req_failed................: 0.00%  ✓ 0         ✗ 1931
http_req_receiving.............: avg=93.7µs  min=51µs   med=85µs    max=826µs  p(90)=119µs   p(95)=144µs
http_req_sending...............: avg=27.88µs min=12µs   med=24µs    max=1.06ms p(90)=37µs    p(95)=48.5µs
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s      max=0s     p(90)=0s      p(95)=0s
http_req_waiting...............: avg=30.74ms min=4.45ms med=23.28ms max=3.03s  p(90)=41.46ms p(95)=56.77ms
http_reqs......................: 1931   32.173551/s
iteration_duration.............: avg=31.05ms min=4.82ms med=23.56ms max=3.03s  p(90)=41.79ms p(95)=57.05ms
iterations.....................: 1931   32.173551/s
vus............................: 1      min=1       max=1
vus_max........................: 1      min=1       max=1

# Время 60 с, количество потоков 10, количество соединений 10, No Cache (MariaDB)

data_received..................: 634 kB 11 kB/s
data_sent......................: 197 kB 3.3 kB/s
http_req_blocked...............: avg=51.93µs  min=1µs     med=4µs      max=11.55ms p(90)=6µs      p(95)=8µs
http_req_connecting............: avg=1.27µs   min=0s      med=0s       max=429µs   p(90)=0s       p(95)=0s
http_req_duration..............: avg=283.92ms min=88.38ms med=231.55ms max=1.52s   p(90)=438.78ms p(95)=621.39ms
{ expected_response:true }...: avg=283.92ms min=88.38ms med=231.55ms max=1.52s   p(90)=438.78ms p(95)=621.39ms
http_req_failed................: 0.00%  ✓ 0         ✗ 2124
http_req_receiving.............: avg=72.71µs  min=18µs    med=64µs     max=1.71ms  p(90)=104µs    p(95)=124µs
http_req_sending...............: avg=22.13µs  min=7µs     med=19µs     max=460µs   p(90)=29µs     p(95)=37.84µs
http_req_tls_handshaking.......: avg=0s       min=0s      med=0s       max=0s      p(90)=0s       p(95)=0s
http_req_waiting...............: avg=283.82ms min=88.26ms med=231.39ms max=1.52s   p(90)=438.72ms p(95)=621.01ms
http_reqs......................: 2124   35.113744/s
iteration_duration.............: avg=284.13ms min=88.48ms med=231.73ms max=1.53s   p(90)=439.26ms p(95)=621.58ms
iterations.....................: 2124   35.113744/s
vus............................: 10     min=10      max=10
vus_max........................: 10     min=10      max=10

# Время 60 с, количество потоков 10, количество соединений 10, Use Cache (MariaDB)

data_received..................: 727 kB 12 kB/s
data_sent......................: 227 kB 3.8 kB/s
http_req_blocked...............: avg=14.78µs  min=2µs     med=4µs      max=3.61ms p(90)=6µs      p(95)=8µs
http_req_connecting............: avg=2.89µs   min=0s      med=0s       max=944µs  p(90)=0s       p(95)=0s
http_req_duration..............: avg=245.99ms min=63.38ms med=221.4ms  max=2.41s  p(90)=355.12ms p(95)=419.72ms
{ expected_response:true }...: avg=245.99ms min=63.38ms med=221.4ms  max=2.41s  p(90)=355.12ms p(95)=419.72ms
http_req_failed................: 0.00%  ✓ 0         ✗ 2439
http_req_receiving.............: avg=77.06µs  min=20µs    med=74µs     max=522µs  p(90)=104µs    p(95)=120µs
http_req_sending...............: avg=24.89µs  min=8µs     med=22µs     max=1ms    p(90)=30µs     p(95)=38µs
http_req_tls_handshaking.......: avg=0s       min=0s      med=0s       max=0s     p(90)=0s       p(95)=0s
http_req_waiting...............: avg=245.89ms min=63.23ms med=221.3ms  max=2.41s  p(90)=354.99ms p(95)=419.59ms
http_reqs......................: 2439   40.590019/s
iteration_duration.............: avg=246.17ms min=63.61ms med=221.56ms max=2.41s  p(90)=355.27ms p(95)=421.06ms
iterations.....................: 2439   40.590019/s
vus............................: 10     min=10      max=10
vus_max........................: 10     min=10      max=10

# Время 60 с, количество потоков 1, количество соединений 1, No Cache (MongoDB)

data_received..................: 2.0 MB 33 kB/s
data_sent......................: 643 kB 11 kB/s
http_req_blocked...............: avg=5.68µs  min=2µs    med=5µs    max=2.87ms   p(90)=7µs     p(95)=9µs     
http_req_connecting............: avg=27ns    min=0s     med=0s     max=193µs    p(90)=0s      p(95)=0s      
http_req_duration..............: avg=8.46ms  min=3.1ms  med=6.56ms max=260.68ms p(90)=13.71ms p(95)=16.19ms 
{ expected_response:true }...: avg=8.46ms  min=3.1ms  med=6.56ms max=260.68ms p(90)=13.71ms p(95)=16.19ms 
http_req_failed................: 0.00%  ✓ 0          ✗ 6919
http_req_receiving.............: avg=93.28µs min=50µs   med=86µs   max=1.92ms   p(90)=113µs   p(95)=132.09µs
http_req_sending...............: avg=25.41µs min=12µs   med=23µs   max=305µs    p(90)=32µs    p(95)=36µs    
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s     max=0s       p(90)=0s      p(95)=0s      
http_req_waiting...............: avg=8.34ms  min=3ms    med=6.45ms max=260.56ms p(90)=13.59ms p(95)=16.06ms 
http_reqs......................: 6919   115.310803/s
iteration_duration.............: avg=8.64ms  min=3.36ms med=6.73ms max=260.82ms p(90)=13.9ms  p(95)=16.39ms 
iterations.....................: 6919   115.310803/s
vus............................: 1      min=1        max=1 
vus_max........................: 1      min=1        max=1 

# Время 60 с, количество потоков 1, количество соединений 1, Use Cache (MongoDB)

data_received..................: 1.9 MB 32 kB/s
data_sent......................: 622 kB 10 kB/s
http_req_blocked...............: avg=5.51µs  min=2µs    med=5µs    max=3.02ms   p(90)=7µs     p(95)=8µs    
http_req_connecting............: avg=38ns    min=0s     med=0s     max=258µs    p(90)=0s      p(95)=0s     
http_req_duration..............: avg=8.76ms  min=2.49ms med=7.25ms max=267.89ms p(90)=12.76ms p(95)=14.83ms
{ expected_response:true }...: avg=8.76ms  min=2.49ms med=7.25ms max=267.89ms p(90)=12.76ms p(95)=14.83ms
http_req_failed................: 0.00%  ✓ 0          ✗ 6698
http_req_receiving.............: avg=89.63µs min=50µs   med=85µs   max=890µs    p(90)=113µs   p(95)=126µs  
http_req_sending...............: avg=24.03µs min=12µs   med=22µs   max=138µs    p(90)=31µs    p(95)=34µs   
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s     max=0s       p(90)=0s      p(95)=0s     
http_req_waiting...............: avg=8.64ms  min=2.4ms  med=7.14ms max=267.36ms p(90)=12.64ms p(95)=14.72ms
http_reqs......................: 6698   111.600543/s
iteration_duration.............: avg=8.93ms  min=2.6ms  med=7.43ms max=268.54ms p(90)=12.97ms p(95)=15.01ms
iterations.....................: 6698   111.600543/s
vus............................: 1      min=1        max=1 
vus_max........................: 1      min=1        max=1 

# Время 60 с, количество потоков 10, количество соединений 10, No Cache (MongoDB)

data_received..................: 4.0 MB 67 kB/s
data_sent......................: 1.3 MB 22 kB/s
http_req_blocked...............: avg=7.62µs  min=1µs    med=4µs     max=5.97ms   p(90)=6µs     p(95)=8µs    
http_req_connecting............: avg=535ns   min=0s     med=0s      max=1.1ms    p(90)=0s      p(95)=0s     
http_req_duration..............: avg=42.2ms  min=7.97ms med=37.7ms  max=444.14ms p(90)=56.91ms p(95)=68.07ms
{ expected_response:true }...: avg=42.2ms  min=7.97ms med=37.7ms  max=444.14ms p(90)=56.91ms p(95)=68.07ms
http_req_failed................: 0.00%  ✓ 0          ✗ 14159
http_req_receiving.............: avg=66.02µs min=18µs   med=60µs    max=2.2ms    p(90)=94µs    p(95)=108µs  
http_req_sending...............: avg=21.36µs min=7µs    med=19µs    max=1.06ms   p(90)=29µs    p(95)=34µs   
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s      max=0s       p(90)=0s      p(95)=0s     
http_req_waiting...............: avg=42.11ms min=7.89ms med=37.61ms max=444.04ms p(90)=56.84ms p(95)=67.96ms
http_reqs......................: 14159  235.846853/s
iteration_duration.............: avg=42.37ms min=8.07ms med=37.86ms max=444.39ms p(90)=57.11ms p(95)=68.27ms
iterations.....................: 14159  235.846853/s
vus............................: 10     min=10       max=10 
vus_max........................: 10     min=10       max=10 

# Время 60 с, количество потоков 10, количество соединений 10, Use Cache (MongoDB)

data_received..................: 2.7 MB 44 kB/s
data_sent......................: 870 kB 15 kB/s
http_req_blocked...............: avg=10.12µs min=1µs    med=5µs     max=7.63ms   p(90)=7µs     p(95)=10µs    
http_req_connecting............: avg=1.38µs  min=0s     med=0s      max=2.02ms   p(90)=0s      p(95)=0s      
http_req_duration..............: avg=63.93ms min=6.04ms med=55.36ms max=589.92ms p(90)=92.63ms p(95)=122.96ms
{ expected_response:true }...: avg=63.93ms min=6.04ms med=55.36ms max=589.92ms p(90)=92.63ms p(95)=122.96ms
http_req_failed................: 0.00%  ✓ 0          ✗ 9364
http_req_receiving.............: avg=79.5µs  min=15µs   med=74µs    max=1.6ms    p(90)=108µs   p(95)=128µs   
http_req_sending...............: avg=25.09µs min=8µs    med=23µs    max=1.63ms   p(90)=33µs    p(95)=41µs    
http_req_tls_handshaking.......: avg=0s      min=0s     med=0s      max=0s       p(90)=0s      p(95)=0s      
http_req_waiting...............: avg=63.82ms min=5.95ms med=55.25ms max=589.79ms p(90)=92.54ms p(95)=122.88ms
http_reqs......................: 9364   155.864842/s
iteration_duration.............: avg=64.11ms min=6.2ms  med=55.54ms max=590.19ms p(90)=92.82ms p(95)=123.54ms
iterations.....................: 9364   155.864842/s
vus............................: 10     min=10       max=10
vus_max........................: 10     min=10       max=10

# Время 60 с, количество потоков 50, количество соединений 50, No Cache (MongoDB)

data_received..................: 4.4 MB 73 kB/s
data_sent......................: 1.4 MB 24 kB/s
http_req_blocked...............: avg=53.66µs  min=1µs     med=3µs      max=36.25ms p(90)=6µs      p(95)=10µs    
http_req_connecting............: avg=5.99µs   min=0s      med=0s       max=3.43ms  p(90)=0s       p(95)=0s      
http_req_duration..............: avg=194.17ms min=60.44ms med=159.31ms max=1.01s   p(90)=325.76ms p(95)=410.92ms
{ expected_response:true }...: avg=194.17ms min=60.44ms med=159.31ms max=1.01s   p(90)=325.76ms p(95)=410.92ms
http_req_failed................: 0.00%  ✓ 0         ✗ 15439
http_req_receiving.............: avg=61.14µs  min=13µs    med=50µs     max=5.57ms  p(90)=89µs     p(95)=113µs   
http_req_sending...............: avg=22.12µs  min=5µs     med=17µs     max=3.56ms  p(90)=30µs     p(95)=41µs    
http_req_tls_handshaking.......: avg=0s       min=0s      med=0s       max=0s      p(90)=0s       p(95)=0s      
http_req_waiting...............: avg=194.08ms min=60.33ms med=159.23ms max=1.01s   p(90)=325.69ms p(95)=410.85ms
http_reqs......................: 15439  257.00702/s
iteration_duration.............: avg=194.38ms min=60.61ms med=159.53ms max=1.01s   p(90)=326.07ms p(95)=411.17ms
iterations.....................: 15439  257.00702/s
vus............................: 50     min=50      max=50 
vus_max........................: 50     min=50      max=50 

# Время 60 с, количество потоков 50, количество соединений 50, Use Cache (MongoDB)

data_received..................: 3.8 MB 62 kB/s
data_sent......................: 1.2 MB 21 kB/s
http_req_blocked...............: avg=38.34µs  min=1µs     med=4µs      max=12.3ms   p(90)=7µs      p(95)=8µs     
http_req_connecting............: avg=9.77µs   min=0s      med=0s       max=4.2ms    p(90)=0s       p(95)=0s      
http_req_duration..............: avg=226.59ms min=41.38ms med=231.79ms max=667.73ms p(90)=312.69ms p(95)=346.92ms
{ expected_response:true }...: avg=226.59ms min=41.38ms med=231.79ms max=667.73ms p(90)=312.69ms p(95)=346.92ms
http_req_failed................: 0.00%  ✓ 0          ✗ 13244
http_req_receiving.............: avg=68.67µs  min=18µs    med=63µs     max=1.35ms   p(90)=99µs     p(95)=115µs   
http_req_sending...............: avg=25.19µs  min=7µs     med=21µs     max=3.56ms   p(90)=31µs     p(95)=36µs    
http_req_tls_handshaking.......: avg=0s       min=0s      med=0s       max=0s       p(90)=0s       p(95)=0s      
http_req_waiting...............: avg=226.5ms  min=41.34ms med=231.7ms  max=667.64ms p(90)=312.52ms p(95)=346.79ms
http_reqs......................: 13244  220.284255/s
iteration_duration.............: avg=226.79ms min=41.47ms med=231.95ms max=667.9ms  p(90)=312.99ms p(95)=347.5ms 
iterations.....................: 13244  220.284255/s
vus............................: 50     min=50       max=50 
vus_max........................: 50     min=50       max=50 