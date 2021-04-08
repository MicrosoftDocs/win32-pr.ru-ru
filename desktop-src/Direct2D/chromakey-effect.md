---
title: Чрома-клавиша
description: Преобразует заданный цвет плюс или минус значение допуска в альфа-канал. Например, чрома-Key может удалить фон изображения для зеленого цвета экрана.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891761"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="c6361-104">Чрома-клавиша</span><span class="sxs-lookup"><span data-stu-id="c6361-104">Chroma-key effect</span></span>

<span data-ttu-id="c6361-105">Преобразует заданный цвет плюс или минус значение допуска в альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="c6361-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="c6361-106">Например, чрома-Key может удалить фон изображения для зеленого цвета экрана.</span><span class="sxs-lookup"><span data-stu-id="c6361-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="c6361-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="c6361-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="c6361-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="c6361-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="c6361-109">Образец кода</span><span class="sxs-lookup"><span data-stu-id="c6361-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="c6361-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="c6361-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c6361-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c6361-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c6361-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c6361-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c6361-113">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="c6361-113">Example image</span></span>

![Пример выходных данных эффектов](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="c6361-115">В этом примере результатом действия чрома-Key является второе изображение с прозрачным фоном шахматной доски.</span><span class="sxs-lookup"><span data-stu-id="c6361-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="c6361-116">Третий образ сочетает это с фоновым изображением для окончательного наложения зеленого экрана.</span><span class="sxs-lookup"><span data-stu-id="c6361-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="c6361-117">Пример кода</span><span class="sxs-lookup"><span data-stu-id="c6361-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="c6361-118">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="c6361-118">Effect properties</span></span>

<span data-ttu-id="c6361-119">Свойства для влияния чрома-Key определяются перечислением [**D2D1 \_ чромакэй \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .</span><span class="sxs-lookup"><span data-stu-id="c6361-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6361-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c6361-120">Requirements</span></span>

| <span data-ttu-id="c6361-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c6361-121">Requirement</span></span> | <span data-ttu-id="c6361-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c6361-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c6361-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6361-123">Minimum supported client</span></span> | <span data-ttu-id="c6361-124">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="c6361-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c6361-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6361-125">Minimum supported server</span></span> | <span data-ttu-id="c6361-126">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="c6361-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c6361-127">Header</span><span class="sxs-lookup"><span data-stu-id="c6361-127">Header</span></span>                   | <span data-ttu-id="c6361-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="c6361-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c6361-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6361-129">Library</span></span>                  | <span data-ttu-id="c6361-130">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="c6361-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="c6361-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c6361-131">Related topics</span></span>

* [<span data-ttu-id="c6361-132">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="c6361-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
