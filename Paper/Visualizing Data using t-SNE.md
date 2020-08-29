## 📋 논문의 정보를 알려주세요.

>- Visualizing Data using t-SNE 
>- Laurens van der Maaten, Geoffrey Hinton
>- 9(Nov):2579--2605, 2008.

## 📃 Abstract
>We present a new technique called "t-SNE" that visualizes high-dimensional data by giving each datapoint a location in a two or three-dimensional map. The technique is a variation of Stochastic Neighbor Embedding (Hinton and Roweis, 2002) that is much easier to optimize, and produces significantly better visualizations by reducing the tendency to crowd points together in the center of the map. t-SNE is better than existing techniques at creating a single map that reveals structure at many different scales. This is particularly important for high-dimensional data that lie on several different, but related, low-dimensional manifolds, such as images ofobjects from multiple classes seen from multiple viewpoints. For visualizing the structure of very large data sets, we show how t-SNE can use random walks on neighborhood graphs to allow the implicit structure of all of the data to influence the way in which a subset of the data is displayed. We illustrate the performance of t-SNE on a wide variety of data sets and compare it with many other non-parametric visualization techniques, including Sammon mapping, Isomap, and Locally Linear Embedding. The visualizations produced by t-SNE are significantly better than those produced by the other techniques on almost all of the data sets.

## 🔎 어떤 논문인지 소개해주세요.
- 논문에서 제안한 Embedding 기법인 SNE는 원공간과 축소된 공간의 유클리디안 거리에 대한 확률을 구하고 확률이 같아지게 update를 하는 알고리즘입니다. 
- SNE는 시각화에 좋은 성능을 보이지만, 비용함수 최적화 문제와 Crowding 문제가 있습니다. 
- 이를 원활하게 하고자 수학적인 테크닉을 이용해서 비용함수를 간소화 시키고 봉우리가 낮고 꼬리가 두터운 student-t분포를 이용해서 Crowding 문제를 보완합니다. 

## 🔑 핵심 키워드를 적어주세요.
- SNE(Stochastic Neighbor Embeding)
- Symmetric SNE
- crowding problem
- student-t distribution

## 📎 URL
>https://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf

## 💡 방법은 무엇입니까?
 
## 📈 실험과 그 결과는 어떻습니까?
> * 실험
  MNIST의 손글씨 데이터, Olivetti의 얼굴 데이터 등의 데이터를 이용해서 다른 embedding 기법인 Sammon mapping, Isomap, LLE랑 비교해서 시각화 성능을 평가했습니다. 

> * 결과


## 📂 차후 연구방향이나 보완점은 무엇입니까?

## 👍 novelty와 논문을 통해 배운 것은 무엇입니까?

## ➿ 궁금한 점이나 추가로 읽으면 좋은 레퍼런스가 있습니까?
