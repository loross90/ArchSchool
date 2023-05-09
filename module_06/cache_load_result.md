# k6 load tests

# Время 60 с, количество потоков 1, количество соединений 1, No Cache

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

# Время 60 с, количество потоков 1, количество соединений 1, Use Cache

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

# Время 60 с, количество потоков 10, количество соединений 10, No Cache

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

# Время 60 с, количество потоков 10, количество соединений 10, Use Cache

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

# Время 60 с, количество потоков 50, количество соединений 50, No Cache



# Время 60 с, количество потоков 50, количество соединений 50, Use Cache

