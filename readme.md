# VO-Evaluation
## Generate eval_train.exe and eval_test.exe
```
$ cd cpp
```
- as for train seq  

uncomment line 424 in evaluate_odometry.cpp, then compile it via
```
$ g++ -O3 -DNDEBUG -o eval_train evaluate_odometry.cpp matrix.cpp
```
- as for test seq  

uncomment line 427 in evaluate_odometry.cpp, then compile it via
```
g++ -O3 -DNDEBUG -o eval_test evaluate_odometry.cpp matrix.cpp
```

## Evaluation
```
$ mkdir ../test_1
$ mkdir ../test_1/prediction
```
copy the predicted poses(03, 04, 05, 06, 07, 10) in test_1/prediction/, then
```
$ eval_test ../test_1
```
the same with train  

## Plot
