## 📋 논문의 정보를 알려주세요.

>- Visualizing Data using t-SNE 
>- Laurens van der Maaten, Geoffrey Hinton
>- 9(Nov):2579--2605, 2008.

## 📃 Abstract
>We present a new technique called "t-SNE" that visualizes high-dimensional data by giving each datapoint a location in a two or three-dimensional map. The technique is a variation of Stochastic Neighbor Embedding (Hinton and Roweis, 2002) that is much easier to optimize, and produces significantly better visualizations by reducing the tendency to crowd points together in the center of the map. t-SNE is better than existing techniques at creating a single map that reveals structure at many different scales. This is particularly important for high-dimensional data that lie on several different, but related, low-dimensional manifolds, such as images ofobjects from multiple classes seen from multiple viewpoints. For visualizing the structure of very large data sets, we show how t-SNE can use random walks on neighborhood graphs to allow the implicit structure of all of the data to influence the way in which a subset of the data is displayed. We illustrate the performance of t-SNE on a wide variety of data sets and compare it with many other non-parametric visualization techniques, including Sammon mapping, Isomap, and Locally Linear Embedding. The visualizations produced by t-SNE are significantly better than those produced by the other techniques on almost all of the data sets.

## 🔎 어떤 논문인지 소개해주세요.
- 논문에서 제안한 SNE(Stochastic Neighbor Embedding)는 원공간과 축소된 공간의 유클리디안 거리에 대한 확률을 구하고 확률이 같아지게 update를 하는 방식의 Embedding 기법입니다.  

- SNE는 시각화에 좋은 성능을 보이지만, 비용함수 최적화 문제와 crowding 문제가 있습니다. 

- 이를 원활하게 하고자 t-SNE(t-Stochastic Neighbor Embedding)를 제시합니다. 

## 🔑 핵심 키워드를 적어주세요.
- SNE(Stochastic Neighbor Embeding)
- Symmetric SNE
- crowding problem
- student-t distribution

## 📎 URL
>https://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf

## 💡 방법은 무엇입니까?
- Symmetric SNE를 이용해서 비용함수를 간소화 시켜 계산복잡도를 낮췄습니다. 
   * Symmetric SNE는 수학적 테크닉입니다.

- student-t분포의 봉우리가 낮고 꼬리가 두터운 성질을 이용해서 crowding 문제를 보완했습니다. 
   * crowding 문제는 거리의 멀고 가까운 개념이 붕괴되는 것을 의미합니다. 
 
## 📈 실험과 그 결과는 어떻습니까?
- 실험

    * MNIST의 손글씨 데이터, Olivetti의 얼굴 데이터 등의 데이터를 이용해서 다른 embedding 기법인 Sammon mapping, Isomap, LLE랑 비교해서 시각화 성능을 평가했습니다. 

- 결과 

    * 검토 중

## 📂 차후 연구방향이나 보완점은 무엇입니까?
- t-SNE는 일반적인 경우에 성능이 불명확하다

    * t-SNE는 데이터 시각화를 목적으로 한 차원축소이기 때문에 일반적인 경우에는 성능이 불명확합니다.

- 차원의 저주

    * t-SNE는 유클리디안 거리를 사용했기 때문에 가까이서 봤을 때 선형이라는 가정을 하고 진행을 하는데 차원의 저주는 차원이 증가할수록 가정이 위배되는 것을 의미합니다. 
  
    * AutoEncoder를 이용해서 비선형 차원축소를 먼저 이용하고 t-SNE를 이용하는 방식으로 보완을 합니다.

- 비용함수가 convex하지 않다.

    * t-SNE를 실행할 때마다 최적화된 파라미터가 달라질 수 있는 문제점이 있습니다. 

## 👍 novelty와 논문을 통해 배운 것은 무엇입니까?
- Embedding기법은 목적에 따라 다르게 만들어지며 이용됨을 알 수 있었습니다. 

- 거리에 대한 확률을 이용해서 알고리즘을 구성하는건 큰 novelty가 있고, 데이터를 보는 관점이 하나 늘었습니다. 

## ➿ 궁금한 점이나 추가로 읽으면 좋은 레퍼런스가 있습니까?
- AutoEncoder에 대해 추가로 알아보면 좋을꺼 같습니다. 
