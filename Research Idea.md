# 研究笔记：环面退化与六函子形式主义
## 研究方向一：从环面簇到平坦环面退化上的六函子结构

### 1. 核心动机与几何背景
环面簇（Toric Varieties）的几何完全由多面体和扇的组合学所控制，因此其上的层理论与六函子结构具有极高的可计算性和清晰的刻画。本方向旨在跨越环面簇的边界，将这一结构推广至更一般的代数簇（例如通过 Grassmannian 等非环面 Fano 簇）。

核心代数工具是**平坦环面退化（Flat Toric Degeneration）**。我们考虑定义在 $\mathbb{A}^1$ 上的平坦族 $\pi: \mathfrak{X} \to \mathbb{A}^1$，满足：
* **一般纤维 (General Fiber)：** 对于 $t \neq 0$，$\mathfrak{X}_t \cong X$ 为目标光滑簇。
* **中心纤维 (Central Fiber)：** $\mathfrak{X}_0 \cong X_\Delta$ 退化为一个环面簇（通常带有奇点，可通过 Newton-Okounkov 体或 Gröbner 退化构造）。

### 2. 六函子系统的形变追踪
研究的焦点在于考察格罗滕迪克六函子系统 $(f_*, f^*, f_!, f^!, \otimes, \mathcal{RHom})$ 如何沿着形变参数 $t$ 发生过渡，并在导出无穷范畴的层面上建立联系。

* **拓扑/可构造层侧：** 考察中心奇异纤维 $\mathfrak{X}_0$ 上的反常层与交截同调复形 $IC_{\mathfrak{X}_0}$。利用近邻闭链函子（Nearby Cycles Functor） $\Psi$，将一般纤维 $\mathfrak{X}_t$ 上的拓扑信息与中心纤维 $X_\Delta$ 上的组合/层论数据建立同调层面的联系。
* **代数/凝聚层侧：** 由于中心环面簇 $X_\Delta$ 往往不可避免地带有奇点，传统的拟凝聚层范畴 $QCoh(\mathfrak{X}_0)$ 无法提供良好的异常拉回 $f^!$ 与对偶理论。研究将基于 Gaitsgory 等人的导出代数几何框架，在代极限定理层无穷范畴 $IndCoh(\mathfrak{X}_0)$ 中重建完美的六函子对应，以此驯服退化产生的特异性。

### 3. 几何与算术应用：Manin 猜想的同调视角
本方向的最终几何落脚点之一，是试图通过同调代数与范畴论的方法，为 Fano 簇上的有理点渐近分布（Manin 猜想）提供新的切入点。
* Batyrev 和 Tschinkel 等人的经典工作已将纯环面簇上的 Manin 猜想完全转化为对多面体体积与极化锥的组合解析计算。
* 通过平坦族 $\mathfrak{X}$，本研究计划追踪计数常数与同调不变量在六函子基变换（Base Change）下的行为，尝试将中心纤维 $X_\Delta$ 上极度成熟的组合层论数据，平滑或通过同伦连贯的代数机制“拉回”到一般纤维 $X$ 上。

## 研究方向三：大一统——利用 Motivic 理论推导退化上的六函子与 $IndCoh$

### 1. 核心构想：以 $SH(-)$ 作为普适图纸
将平坦环面退化 $\pi: \mathfrak{X} \to \mathbb{A}^1$ 提升到稳定 $\infty$-范畴的动机层面上。
不直接在奇异的中心纤维 $\mathfrak{X}_0$ 上硬算凝聚层的六函子，而是先在动机范畴 $SH(\mathfrak{X})$ 中利用 Cisinski-Déglise 和 Ayoub 的动机六函子形式主义建立几何框架。由于 $SH(-)$ 满足极其良好的下降条件和 $\mathbb{A}^1$-同伦不变性，它能最大程度地屏蔽中心纤维的病态代数奇点。

### 2. 动机近邻闭链 (Motivic Nearby Cycles) 与组合局部化
* **核心工具：** 引入 Ayoub 的动机近邻闭链函子 $\Psi_{mot}: SH(\mathfrak{X}_\eta) \to SH(\mathfrak{X}_0)$。
* **环面优势：** 利用中心纤维 $\mathfrak{X}_0 \cong X_\Delta$（环面簇）的轨道分层（Orbit Stratification）。由于环面簇的动机是纯泰特型的（Tate type），我们可以将高度非线性的 $\Psi_{mot}$ 在 $SH(X_\Delta)$ 中的行为，彻底拆解为沿着多面体面（Faces）的组合六函子运算（如基于轨道的 $i_*$ 和 $i^!$ 粘合）。

### 3. 从 Motivic 到 $IndCoh$ 的范畴化实现 (Categorical Realization)
* 利用高阶范畴论中的实现函子（Realization Functors），将 $SH(\mathfrak{X}_0)$ 上已经通过多面体组合学算清楚的六函子关系，平滑“下推”或“映射”到导出代数几何的 $IndCoh(\mathfrak{X}_0)$ 或 $\mathcal{D}\text{-mod}(\mathfrak{X}_0)$ 范畴中。
* **最终目的：** 证明一般纤维（如 Grassmannian）上的 $IndCoh$ 结构，可以完全由其退化的环面簇上的多面体数据，通过范畴化的近邻闭链和 Motivic 滤子来重构。这为研究 Fano 簇的同调镜像对称（HMS）和 Manin 猜想提供了一套全新的、完全可计算的代数几何 $\infty$-机器。