---
title: Эффект перекрестной плавности
description: Этот результат сочетает два изображения, добавляя взвешенные Пиксели из входных изображений. Он имеет два входа, именуемые Destination и Source.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534115"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="694db-104">Эффект перекрестной плавности</span><span class="sxs-lookup"><span data-stu-id="694db-104">Cross-fade effect</span></span>

<span data-ttu-id="694db-105">Этот результат сочетает два изображения, добавляя взвешенные Пиксели из входных изображений.</span><span class="sxs-lookup"><span data-stu-id="694db-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="694db-106">Он имеет два входа, именуемые Destination и Source.</span><span class="sxs-lookup"><span data-stu-id="694db-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="694db-107">Формула перекрестного перезатухания — это **Output = вес \* назначения + (1-вес) \* источник**.</span><span class="sxs-lookup"><span data-stu-id="694db-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="694db-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="694db-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="694db-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="694db-109">Effect properties</span></span>

| <span data-ttu-id="694db-110">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="694db-110">Display name and index enumeration</span></span>             | <span data-ttu-id="694db-111">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="694db-111">Type and default value</span></span> | <span data-ttu-id="694db-112">Описание</span><span class="sxs-lookup"><span data-stu-id="694db-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="694db-113">WeightD2D1 — \_ \_ вес Prop \_</span><span class="sxs-lookup"><span data-stu-id="694db-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="694db-114">FLOAT 0,5 f</span><span class="sxs-lookup"><span data-stu-id="694db-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="694db-115">Степень подсистемы значений цветов исходного изображения относительно целевого изображения.</span><span class="sxs-lookup"><span data-stu-id="694db-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="694db-116">Минимальное значение — 0,0 f (для определения выходных данных используется монопольный образ назначения), а максимальное значение — 1,0 f (для определения выходных данных используется монопольное использование исходного образа).</span><span class="sxs-lookup"><span data-stu-id="694db-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="694db-117">Требования</span><span class="sxs-lookup"><span data-stu-id="694db-117">Requirements</span></span>



| <span data-ttu-id="694db-118">Требование</span><span class="sxs-lookup"><span data-stu-id="694db-118">Requirement</span></span> | <span data-ttu-id="694db-119">Значение</span><span class="sxs-lookup"><span data-stu-id="694db-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="694db-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="694db-120">Minimum supported client</span></span> | <span data-ttu-id="694db-121">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="694db-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="694db-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="694db-122">Minimum supported server</span></span> | <span data-ttu-id="694db-123">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="694db-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="694db-124">Header</span><span class="sxs-lookup"><span data-stu-id="694db-124">Header</span></span>                   | <span data-ttu-id="694db-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="694db-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="694db-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="694db-126">Library</span></span>                  | <span data-ttu-id="694db-127">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="694db-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="694db-128">См. также</span><span class="sxs-lookup"><span data-stu-id="694db-128">Related topics</span></span>

* [<span data-ttu-id="694db-129">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="694db-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
