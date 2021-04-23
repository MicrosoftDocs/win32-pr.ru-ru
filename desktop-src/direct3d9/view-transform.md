---
description: В этом разделе описываются основные понятия преобразования представления и приводятся подробные сведения о настройке матрицы преобразования представления в приложении Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Преобразование представления (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537583"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="4546a-103">Преобразование представления (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4546a-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="4546a-104">В этом разделе описываются основные понятия преобразования представления и приводятся подробные сведения о настройке матрицы преобразования представления в приложении Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4546a-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="4546a-105">Видовое преобразование определяет положение наблюдателя в мировом пространстве и обеспечивает преобразование вершин в пространство камеры.</span><span class="sxs-lookup"><span data-stu-id="4546a-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="4546a-106">В пространстве камеры камера, или наблюдатель, находится в начале координат и смотрит в направлении положительной полуоси Z.</span><span class="sxs-lookup"><span data-stu-id="4546a-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="4546a-107">Вспомним, что Direct3D использует левую систему координат, поэтому z является положительным в сцене.</span><span class="sxs-lookup"><span data-stu-id="4546a-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="4546a-108">Видовая матрица переносит объекты в мировом пространстве относительно положения камеры — начала координат пространства камеры — и ориентации камеры.</span><span class="sxs-lookup"><span data-stu-id="4546a-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="4546a-109">Существует множество способов создания видовой матрицы.</span><span class="sxs-lookup"><span data-stu-id="4546a-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="4546a-110">Во всех случаях камера имеет некоторые логическое положение и ориентацию в мировом пространстве, которые используются в качестве начальной точки для создания видовой матрицы, которая будет применяться к моделям в сцене.</span><span class="sxs-lookup"><span data-stu-id="4546a-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="4546a-111">Видовая матрица параллельно переносит и поворачивает объекты, чтобы поместить их в пространство камеры, где камера находится в начале координат.</span><span class="sxs-lookup"><span data-stu-id="4546a-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="4546a-112">Один из способов создания видовой матрицы — это сочетание матрицы параллельного переноса с матрицами поворота для каждой оси.</span><span class="sxs-lookup"><span data-stu-id="4546a-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="4546a-113">При таком подходе применяется следующее общее матричное уравнение.</span><span class="sxs-lookup"><span data-stu-id="4546a-113">In this approach, the following general matrix equation applies.</span></span>

![уравнение видового преобразования](images/viewtran.png)

<span data-ttu-id="4546a-115">В этой формуле V — это создаваемая видовая матрица, T — матрица параллельного переноса, которая перемещает объекты в мире, а Rₓ – R<sub>z</sub> — матрицы поворота, которые поворачивают объекты вокруг осей X, Y и Z.</span><span class="sxs-lookup"><span data-stu-id="4546a-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="4546a-116">Матрицы параллельного переноса и поворота основываются на логическом положении и ориентации камеры в мировом пространстве.</span><span class="sxs-lookup"><span data-stu-id="4546a-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="4546a-117">Таким образом, если логическая координата камеры в мире <10, 20100>, целью матрицы перевода является перемещение объектов — 10 единиц вдоль оси x, 20 единиц вдоль оси y и-100 единиц вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="4546a-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="4546a-118">Матрицы поворота в формуле основываются на ориентации камеры — на том, насколько оси пространства камеры повернуты по отношению к мировому пространству.</span><span class="sxs-lookup"><span data-stu-id="4546a-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="4546a-119">Например, если упомянутая выше камера направлена прямо вниз, ее ось Z на 90 градусов (пи/2 радиана) повернута относительно оси Z мирового пространства, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="4546a-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![иллюстрация видового пространства камеры в сравнении с мировым пространством](images/camtop.png)

<span data-ttu-id="4546a-121">Матрицы поворота применяют повороты равной — но противоположной — величины к моделям в сцене.</span><span class="sxs-lookup"><span data-stu-id="4546a-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="4546a-122">Видовая матрица для этой камеры предполагает поворот на –90 градусов вокруг оси X.</span><span class="sxs-lookup"><span data-stu-id="4546a-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="4546a-123">Матрица поворота объединяется с параллельного переноса для создания видовой матрицы, которая корректирует положение и ориентацию объектов в сцене так, что их верх обращен к камере, создавая впечатление, что камера находится над моделью.</span><span class="sxs-lookup"><span data-stu-id="4546a-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="4546a-124">Установка видовой матрицы</span><span class="sxs-lookup"><span data-stu-id="4546a-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="4546a-125">Вспомогательные функции [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) и [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) создают матрицу представления на основе расположения камеры и точки просмотра.</span><span class="sxs-lookup"><span data-stu-id="4546a-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="4546a-126">В следующем примере создается матрица представления для координат левой части.</span><span class="sxs-lookup"><span data-stu-id="4546a-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="4546a-127">Direct3D использует мировую матрицу и видовую матрицу для конфигурирования нескольких внутренних структур данных.</span><span class="sxs-lookup"><span data-stu-id="4546a-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="4546a-128">Каждый раз, когда вы устанавливаете новую мировую или видовую матрицу, система пересчитывает соответствующие внутренние структуры.</span><span class="sxs-lookup"><span data-stu-id="4546a-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="4546a-129">Частая установка этих матриц занимает много вычислительного времени.</span><span class="sxs-lookup"><span data-stu-id="4546a-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="4546a-130">Свести к минимуму количество необходимых вычислений можно путем конкатенации мировой и видовой матриц в мировую-видовую матрицу, задать ее в качестве мировой матрицы, а затем установить видовую матрицу в единичную.</span><span class="sxs-lookup"><span data-stu-id="4546a-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="4546a-131">Сохраняйте кэшированные копии отдельных мировых и видовых матриц, чтобы вы могли изменять, объединять и сбрасывать мировую матрицу по необходимости.</span><span class="sxs-lookup"><span data-stu-id="4546a-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="4546a-132">Для ясности примеры редко используют эту оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="4546a-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4546a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4546a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4546a-134">Преобразования</span><span class="sxs-lookup"><span data-stu-id="4546a-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



