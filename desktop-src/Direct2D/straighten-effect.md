---
title: Результат выпрямления
description: Поворачивает и при необходимости масштабирует изображение.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554419"
---
# <a name="straighten-effect"></a><span data-ttu-id="cd929-103">Результат выпрямления</span><span class="sxs-lookup"><span data-stu-id="cd929-103">Straighten effect</span></span>

<span data-ttu-id="cd929-104">Поворачивает и при необходимости масштабирует изображение.</span><span class="sxs-lookup"><span data-stu-id="cd929-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="cd929-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Straighten.</span><span class="sxs-lookup"><span data-stu-id="cd929-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="cd929-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="cd929-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="cd929-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="cd929-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="cd929-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="cd929-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="cd929-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cd929-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cd929-110">См. также</span><span class="sxs-lookup"><span data-stu-id="cd929-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="cd929-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="cd929-111">Example image</span></span>

![Пример выходных данных эффектов](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="cd929-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="cd929-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="cd929-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="cd929-114">Effect properties</span></span>

<span data-ttu-id="cd929-115">Свойства для эффектов выпрямления определяются перечислением [**D2D1 \_ выпрямление \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) .</span><span class="sxs-lookup"><span data-stu-id="cd929-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd929-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cd929-116">Requirements</span></span>



| <span data-ttu-id="cd929-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cd929-117">Requirement</span></span> | <span data-ttu-id="cd929-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cd929-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="cd929-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd929-119">Minimum supported client</span></span> | <span data-ttu-id="cd929-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="cd929-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cd929-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd929-121">Minimum supported server</span></span> | <span data-ttu-id="cd929-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="cd929-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cd929-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd929-123">Header</span></span>                   | <span data-ttu-id="cd929-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="cd929-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="cd929-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd929-125">Library</span></span>                  | <span data-ttu-id="cd929-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="cd929-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="cd929-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cd929-127">Related topics</span></span>

* [<span data-ttu-id="cd929-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="cd929-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

