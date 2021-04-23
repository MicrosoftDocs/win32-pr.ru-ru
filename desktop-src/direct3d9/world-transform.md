---
description: Обсуждение мирового преобразования представляет основные понятия и предоставляет подробные сведения о настройке универсального преобразования.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Универсальное преобразование (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416497"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="fe1f9-103">Универсальное преобразование (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fe1f9-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="fe1f9-104">Обсуждение мирового преобразования представляет основные понятия и предоставляет подробные сведения о настройке универсального преобразования.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="fe1f9-105">Что такое универсальное преобразование?</span><span class="sxs-lookup"><span data-stu-id="fe1f9-105">What Is a World Transform?</span></span>

<span data-ttu-id="fe1f9-106">Преобразование «мир» изменяет координаты из пространства модели, где вершины определяются по отношению к локальному источнику модели, к мировому пространству, где вершины определяются относительно источника, общего для всех объектов в сцене.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="fe1f9-107">По сути, мировое преобразование помещает модель в мир, — отсюда и название.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="fe1f9-108">На следующей схеме показана взаимосвязь между мировой системой координат и локальной системой координат модели.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![схема взаимосвязи между мировыми координатами и локальными координатами](images/worldcrd.png)

<span data-ttu-id="fe1f9-110">Мировое преобразование может включать любое сочетание параллельных переносов, поворотов и масштабирований.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="fe1f9-111">Установка мировой матрицы</span><span class="sxs-lookup"><span data-stu-id="fe1f9-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="fe1f9-112">Как и в случае с любыми другими преобразованиями, мировое преобразование создается путем с конкатенации ряда матриц в единую матрицу, которая содержит всю сумму их эффектов.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="fe1f9-113">В самом простом случае, когда модель находится в мировом начале координат и ее локальные координатные оси ориентированы так же, как мировое пространство, мировая матрица представляет собой единичную матрицу.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="fe1f9-114">Чаще, однако, мировая матрица представляет собой сочетание параллельного переноса в мировое пространство и, возможно, одного или нескольких поворотов для придания модели необходимой ориентации.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="fe1f9-115">В следующем примере из вымышленного класса трехмерной модели, написанного на языке C++, используются вспомогательные функции, включенные в библиотеку служебной программы D3DX, для создания матрицы мира, которая включает три поворота для ориентации модели и перевод, чтобы переместить его относительно его положения в мировом пространстве.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="fe1f9-116">После подготовки матрицы мира вызовите метод [**IDirect3DDevice9:: сеттрансформ**](/windows/desktop/api) , чтобы задать его, указав для первого параметра макрос [**D3DTS \_ World**](d3dts-world.md) .</span><span class="sxs-lookup"><span data-stu-id="fe1f9-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="fe1f9-117">Direct3D использует установленные вами мировую матрицу и видовую матрицу для конфигурирования нескольких внутренних структур данных.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="fe1f9-118">Каждый раз, когда вы устанавливаете новую мировую или видовую матрицу, система пересчитывает соответствующие внутренние структуры.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="fe1f9-119">Частая установка этих матриц — например, несколько тысяч раз на кадр — занимает много вычислительного времени.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="fe1f9-120">Свести к минимуму количество необходимых вычислений можно путем конкатенации мировой и видовой матриц в мировую-видовую матрицу, задать ее в качестве мировой матрицы, а затем установить видовую матрицу в единичную.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="fe1f9-121">Сохраняйте кэшированные копии отдельных мировых и видовых матриц, чтобы вы могли изменять, объединять и сбрасывать мировую матрицу по необходимости.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="fe1f9-122">Для ясности в этой документации примеры Direct3D редко используют эту оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fe1f9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="fe1f9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe1f9-124">Преобразования</span><span class="sxs-lookup"><span data-stu-id="fe1f9-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



