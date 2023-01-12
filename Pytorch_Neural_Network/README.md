# Additional Notes

|About|
|:---|
|requires_grad = True / False|
|grad|
|backward( )|
|step( )|


<br>

## requires_grad = True / False

```py
params = torch.tensor([1.0, 0.0], requires_grad = True)
```

requires_grad가 True인 경우 변수 params에 가해지는 연산의 결과로 만들어지는 모든 텐서를 이은 전체 트리를 기록하라고 Pytorch에 요청하는 것


## grad

```py
params.grad
```

미분값이 params 텐서의 grad 속성에 저장.


## backward()

```py
training_loss.backward()
```

위 함수 호출 시, Optimizer에 전달된 파라미터인 grad가 말단 노드들에 누적


## step()

```py
optimizer.step()
```

optimizer.step() 호출 시, 각 파라미터를 순회하며 grad 속성에 저장된 비율만큼 값 조정


_Refer to 224p_

