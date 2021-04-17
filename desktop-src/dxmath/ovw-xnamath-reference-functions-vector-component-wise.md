---
description: Содержит список функций-векторов, ориентированных на компонент.
ms.assetid: f5464614-f6bb-427d-5488-3ba0fd4c6e8d
title: Функции с векторным компонентом
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7bae881827e0662a06c46dd54971ce5ed591d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711514"
---
# <a name="component-wise-vector-functions"></a><span data-ttu-id="db123-103">Функции с векторным компонентом</span><span class="sxs-lookup"><span data-stu-id="db123-103">Component-wise vector functions</span></span>

<span data-ttu-id="db123-104">Содержит список функций-векторов, ориентированных на компонент.</span><span class="sxs-lookup"><span data-stu-id="db123-104">Lists the component-wise vector functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="db123-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="db123-105">In this section</span></span>



| <span data-ttu-id="db123-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="db123-106">Topic</span></span>                                                             | <span data-ttu-id="db123-107">Описание</span><span class="sxs-lookup"><span data-stu-id="db123-107">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db123-108">**ксмвекторинсерт**</span><span class="sxs-lookup"><span data-stu-id="db123-108">**XMVectorInsert**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert)<br/>               | <span data-ttu-id="db123-109">Поворачивает вектор влево на заданное число 32-разрядных компонентов и вставляет выбранные элементы этого результата в другой вектор.</span><span class="sxs-lookup"><span data-stu-id="db123-109">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span><br/> |
| [<span data-ttu-id="db123-110">**ксмвектормержекси**</span><span class="sxs-lookup"><span data-stu-id="db123-110">**XMVectorMergeXY**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectormergexy)<br/>             | <span data-ttu-id="db123-111">Создает новый вектор, объединяя компоненты x и y двух векторов.</span><span class="sxs-lookup"><span data-stu-id="db123-111">Creates a new vector by combining the x and y-components of two vectors.</span></span><br/>                                                      |
| [<span data-ttu-id="db123-112">**ксмвектормержезв**</span><span class="sxs-lookup"><span data-stu-id="db123-112">**XMVectorMergeZW**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectormergezw)<br/>             | <span data-ttu-id="db123-113">Создает новый вектор, комбинируя z и w-компоненты двух векторов.</span><span class="sxs-lookup"><span data-stu-id="db123-113">Creates a new vector by combining the z and w-components of two vectors.</span></span><br/>                                                      |
| [<span data-ttu-id="db123-114">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="db123-114">**XMVectorPermute**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)<br/>             | <span data-ttu-id="db123-115">Пермутес компоненты двух векторов для создания нового вектора.</span><span class="sxs-lookup"><span data-stu-id="db123-115">Permutes the components of two vectors to create a new vector.</span></span><br/>                                                                |
| [<span data-ttu-id="db123-116">**ксмвекторротателефт**</span><span class="sxs-lookup"><span data-stu-id="db123-116">**XMVectorRotateLeft**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)<br/>       | <span data-ttu-id="db123-117">Поворачивает вектор влево на заданное число 32-разрядных элементов.</span><span class="sxs-lookup"><span data-stu-id="db123-117">Rotates the vector left by a given number of 32-bit elements.</span></span><br/>                                                                 |
| [<span data-ttu-id="db123-118">**ксмвекторротатеригхт**</span><span class="sxs-lookup"><span data-stu-id="db123-118">**XMVectorRotateRight**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright)<br/>     | <span data-ttu-id="db123-119">Поворачивает вектор вправо на заданное число 32-разрядных элементов.</span><span class="sxs-lookup"><span data-stu-id="db123-119">Rotates the vector right by a given number of 32-bit elements.</span></span><br/>                                                                |
| [<span data-ttu-id="db123-120">**ксмвекторселект**</span><span class="sxs-lookup"><span data-stu-id="db123-120">**XMVectorSelect**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorselect)<br/>               | <span data-ttu-id="db123-121">Выполняет выбор каждого компонента между двумя входными векторами и возвращает результирующий вектор.</span><span class="sxs-lookup"><span data-stu-id="db123-121">Performs a per-component selection between two input vectors and returns the resulting vector.</span></span><br/>                                |
| [<span data-ttu-id="db123-122">**ксмвекторселектконтрол**</span><span class="sxs-lookup"><span data-stu-id="db123-122">**XMVectorSelectControl**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorselectcontrol)<br/> | <span data-ttu-id="db123-123">Определяет вектор управления для использования в [**ксмвекторселект**](/windows/win32/api/directxmath/nf-directxmath-xmvectorselect).</span><span class="sxs-lookup"><span data-stu-id="db123-123">Defines a control vector for use in [**XMVectorSelect**](/windows/win32/api/directxmath/nf-directxmath-xmvectorselect).</span></span><br/>                                                 |
| [<span data-ttu-id="db123-124">**ксмвекторшифтлефт**</span><span class="sxs-lookup"><span data-stu-id="db123-124">**XMVectorShiftLeft**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft)<br/>         | <span data-ttu-id="db123-125">Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.</span><span class="sxs-lookup"><span data-stu-id="db123-125">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span><br/>   |
| [<span data-ttu-id="db123-126">**ксмвекторсплатв**</span><span class="sxs-lookup"><span data-stu-id="db123-126">**XMVectorSplatW**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw)<br/>               | <span data-ttu-id="db123-127">Реплицирует компонент «w» вектора в все компоненты.</span><span class="sxs-lookup"><span data-stu-id="db123-127">Replicates the w component of a vector to all of the components.</span></span><br/>                                                              |
| [<span data-ttu-id="db123-128">**ксмвекторсплаткс**</span><span class="sxs-lookup"><span data-stu-id="db123-128">**XMVectorSplatX**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx)<br/>               | <span data-ttu-id="db123-129">Реплицирует компонент x вектора во все компоненты.</span><span class="sxs-lookup"><span data-stu-id="db123-129">Replicates the x component of a vector to all of the components.</span></span><br/>                                                              |
| [<span data-ttu-id="db123-130">**ксмвекторсплати**</span><span class="sxs-lookup"><span data-stu-id="db123-130">**XMVectorSplatY**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty)<br/>               | <span data-ttu-id="db123-131">Реплицирует компонент y вектора во все компоненты.</span><span class="sxs-lookup"><span data-stu-id="db123-131">Replicates the y component of a vector to all of the components.</span></span><br/>                                                              |
| [<span data-ttu-id="db123-132">**ксмвекторсплатз**</span><span class="sxs-lookup"><span data-stu-id="db123-132">**XMVectorSplatZ**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)<br/>               | <span data-ttu-id="db123-133">Реплицирует компонент z вектора на все компоненты.</span><span class="sxs-lookup"><span data-stu-id="db123-133">Replicates the z component of a vector to all of the components.</span></span><br/>                                                              |
| [<span data-ttu-id="db123-134">**ксмвекторсвиззле**</span><span class="sxs-lookup"><span data-stu-id="db123-134">**XMVectorSwizzle**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle)<br/>             | <span data-ttu-id="db123-135">Свиззлес вектор.</span><span class="sxs-lookup"><span data-stu-id="db123-135">Swizzles a vector.</span></span><br/>                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="db123-136">См. также</span><span class="sxs-lookup"><span data-stu-id="db123-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db123-137">Функции векторной библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="db123-137">DirectXMath Library Vector Functions</span></span>](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
