---
title: Эффекты оттенков серого
description: Преобразовывает изображение с использованием монохромных серых оттенков.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802627"
---
# <a name="grayscale-effect"></a><span data-ttu-id="b6293-103">Эффекты оттенков серого</span><span class="sxs-lookup"><span data-stu-id="b6293-103">Grayscale effect</span></span>

<span data-ttu-id="b6293-104">Преобразовывает изображение с использованием монохромных серых оттенков.</span><span class="sxs-lookup"><span data-stu-id="b6293-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="b6293-105">В градациях серого используется Цветовая матрица для преобразования в градации серого с использованием следующей матрицы:</span><span class="sxs-lookup"><span data-stu-id="b6293-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![Матрица преобразования](images/grayscale-effect-matrix.png)

<span data-ttu-id="b6293-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="b6293-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="b6293-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b6293-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="b6293-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b6293-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b6293-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b6293-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b6293-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b6293-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b6293-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b6293-112">Example image</span></span>

![Пример выходных данных эффектов](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="b6293-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b6293-114">Effect properties</span></span>

<span data-ttu-id="b6293-115">У этого действия нет свойств.</span><span class="sxs-lookup"><span data-stu-id="b6293-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6293-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b6293-116">Requirements</span></span>



| <span data-ttu-id="b6293-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b6293-117">Requirement</span></span> | <span data-ttu-id="b6293-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b6293-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b6293-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6293-119">Minimum supported client</span></span> | <span data-ttu-id="b6293-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="b6293-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b6293-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6293-121">Minimum supported server</span></span> | <span data-ttu-id="b6293-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="b6293-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b6293-123">Header</span><span class="sxs-lookup"><span data-stu-id="b6293-123">Header</span></span>                   | <span data-ttu-id="b6293-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b6293-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b6293-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6293-125">Library</span></span>                  | <span data-ttu-id="b6293-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="b6293-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="b6293-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b6293-127">Related topics</span></span>

* [<span data-ttu-id="b6293-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="b6293-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
