---
description: Библиотека служебной программы D3DX предоставляет интерфейс ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Стеки матриц (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894773"
---
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="e86e6-103">Стеки матриц (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e86e6-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="e86e6-104">Библиотека служебной программы D3DX предоставляет интерфейс [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e6-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="e86e6-105">Он предоставляет механизм для включения и выталкивания матрицы в стеке матрицы.</span><span class="sxs-lookup"><span data-stu-id="e86e6-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="e86e6-106">Реализация стека матрицы — это эффективный способ для трассировки матриц во время прохода по иерархии преобразований.</span><span class="sxs-lookup"><span data-stu-id="e86e6-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="e86e6-107">Библиотека служебной программы D3DX использует стек матриц для хранения преобразований в виде матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="e86e6-108">Различные методы интерфейса [**ID3DXMATRIXStack**](id3dxmatrixstack.md) связаны с текущей матрицей или с матрицей, расположенной поверх стека.</span><span class="sxs-lookup"><span data-stu-id="e86e6-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="e86e6-109">Вы можете очистить текущую матрицу с помощью метода [**ID3DXMATRIXStack:: лоадидентити**](id3dxmatrixstack--loadidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e6-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="e86e6-110">Чтобы явно указать определенную матрицу для загрузки в качестве текущей матрицы преобразования, используйте метод [**ID3DXMATRIXStack:: лоадматрикс**](id3dxmatrixstack--loadmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e6-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="e86e6-111">Затем можно вызвать метод [**ID3DXMATRIXStack:: мултматрикс**](id3dxmatrixstack--multmatrix.md) или метод [**ID3DXMATRIXStack:: мултматрикслокал**](id3dxmatrixstack--multmatrixlocal.md) для умножения текущей матрицы на указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e86e6-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="e86e6-112">Метод [**ID3DXMATRIXStack::P Op**](id3dxmatrixstack--pop.md) позволяет вернуться к предыдущей матрице преобразования, а метод [**ID3DXMATRIXStack::P тельную**](id3dxmatrixstack--push.md) добавляет матрицу преобразования в стек.</span><span class="sxs-lookup"><span data-stu-id="e86e6-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="e86e6-113">Отдельные матрицы в стеке матрицы представлены как однородные матрицы 4x4, определяемые структурой [**D3DXMATRIX**](d3dxmatrix.md) библиотеки служебной программы D3DX.</span><span class="sxs-lookup"><span data-stu-id="e86e6-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="e86e6-114">Библиотека служебной программы D3DX предоставляет стек матрицы через объект модели COM.</span><span class="sxs-lookup"><span data-stu-id="e86e6-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="e86e6-115">Реализация иерархии сцены</span><span class="sxs-lookup"><span data-stu-id="e86e6-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="e86e6-116">Стек матриц упрощает создание иерархических моделей, в которых сложные объекты формируются из ряда более простых объектов.</span><span class="sxs-lookup"><span data-stu-id="e86e6-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="e86e6-117">Сцена (или преобразование) обычно представляется древовидной структурой данных.</span><span class="sxs-lookup"><span data-stu-id="e86e6-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="e86e6-118">Каждый узел в древовидной структуре данных содержит матрицу.</span><span class="sxs-lookup"><span data-stu-id="e86e6-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="e86e6-119">Конкретная матрица представляет изменение в системах координат из родительского узла узлов узла.</span><span class="sxs-lookup"><span data-stu-id="e86e6-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="e86e6-120">Например, при моделировании человека вы можете реализовать иерархию, показанную на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e86e6-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![схема иерархии человеческих рычагов](images/stack1.png)

<span data-ttu-id="e86e6-122">В этой иерархии текстовая матрица помещает текст в мир.</span><span class="sxs-lookup"><span data-stu-id="e86e6-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="e86e6-123">Матрица Упперарм содержит поворот наплеча, матрица Ловерарм содержит поворот уступа, а матрица «рука» содержит поворот ладони.</span><span class="sxs-lookup"><span data-stu-id="e86e6-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="e86e6-124">Чтобы определить, где находится рука относительно мира, можно умножить все матрицы от тела вниз до руки.</span><span class="sxs-lookup"><span data-stu-id="e86e6-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="e86e6-125">Предыдущая иерархия имеет более простую упрощенную структуру, поскольку каждый узел имеет только один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="e86e6-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="e86e6-126">Если вы начинаете моделировать руку более подробно, вам, вероятно, придется добавить пальцы и бегунок.</span><span class="sxs-lookup"><span data-stu-id="e86e6-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="e86e6-127">Каждая цифра может быть добавлена в иерархию как дочерние элементы руки, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e86e6-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![схема иерархии человеческого руки](images/stack2.png)

<span data-ttu-id="e86e6-129">Если вы просматриваете весь граф ARM в порядке возрастания по глубине — обход по одному пути до перехода к следующему пути — для рисования сцены, вы выполняете последовательность сегментированной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="e86e6-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="e86e6-130">Например, чтобы визуализировать руки и пальцы, необходимо реализовать следующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="e86e6-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="e86e6-131">Отправьте матрицу руки в стек матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="e86e6-132">Нарисуйте руку.</span><span class="sxs-lookup"><span data-stu-id="e86e6-132">Draw the hand.</span></span>
3.  <span data-ttu-id="e86e6-133">Передача матрицы Thumb в стек матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="e86e6-134">Нарисуйте бегунок.</span><span class="sxs-lookup"><span data-stu-id="e86e6-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="e86e6-135">Откройте матрицу Thumb из стека.</span><span class="sxs-lookup"><span data-stu-id="e86e6-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="e86e6-136">Перетащите матрицу Finger 1 в стек матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="e86e6-137">Нарисуйте первый палец.</span><span class="sxs-lookup"><span data-stu-id="e86e6-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="e86e6-138">Откройте матрицу с пальцем 1 из стека.</span><span class="sxs-lookup"><span data-stu-id="e86e6-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="e86e6-139">Помещает матрицу Finger 2 в стек матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="e86e6-140">Вы продолжите таким образом, пока не будут отображены все пальцы и бегунок.</span><span class="sxs-lookup"><span data-stu-id="e86e6-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="e86e6-141">После завершения подготовки к просмотру пальцев можно будет отключать матрицу «рука» из стека.</span><span class="sxs-lookup"><span data-stu-id="e86e6-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="e86e6-142">Этот базовый процесс можно выполнить в коде с помощью следующих примеров.</span><span class="sxs-lookup"><span data-stu-id="e86e6-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="e86e6-143">Когда вы сталкиваетесь с узлом во время поиска в структуре дерева данных по глубину, помещаете матрицу на вершину стека матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="e86e6-144">Завершив работу с узлом, разверните матрицу, расположенную на вершине стека матриц.</span><span class="sxs-lookup"><span data-stu-id="e86e6-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="e86e6-145">Таким образом, матрица в верхней части стека всегда представляет мировое преобразование текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e86e6-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="e86e6-146">Поэтому перед рисованием каждого узла необходимо задать матрицу Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e86e6-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="e86e6-147">Дополнительные сведения о конкретных методах, которые можно выполнить в стеке матрицы D3DX, см. в разделе Справочник по [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e6-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e86e6-148">См. также</span><span class="sxs-lookup"><span data-stu-id="e86e6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86e6-149">Конвейер вершин</span><span class="sxs-lookup"><span data-stu-id="e86e6-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



