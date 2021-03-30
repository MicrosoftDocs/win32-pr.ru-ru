---
title: Выцветшей, результат
description: Преобразовывает изображение с использованием оттенков сепии.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988537"
---
# <a name="sepia-effect"></a><span data-ttu-id="dffd8-103">Выцветшей, результат</span><span class="sxs-lookup"><span data-stu-id="dffd8-103">Sepia effect</span></span>

<span data-ttu-id="dffd8-104">Преобразовывает изображение с использованием оттенков сепии.</span><span class="sxs-lookup"><span data-stu-id="dffd8-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="dffd8-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="dffd8-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="dffd8-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="dffd8-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="dffd8-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="dffd8-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="dffd8-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="dffd8-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="dffd8-109">Требования</span><span class="sxs-lookup"><span data-stu-id="dffd8-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="dffd8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="dffd8-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="dffd8-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="dffd8-111">Example image</span></span>

![Пример выходных данных эффектов](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="dffd8-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="dffd8-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="dffd8-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="dffd8-114">Effect properties</span></span>

<span data-ttu-id="dffd8-115">Свойства для выцветшейного действия определяются перечислением [**D2D1 \_ выцветшей \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .</span><span class="sxs-lookup"><span data-stu-id="dffd8-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffd8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dffd8-116">Requirements</span></span>



| <span data-ttu-id="dffd8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dffd8-117">Requirement</span></span> | <span data-ttu-id="dffd8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dffd8-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="dffd8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dffd8-119">Minimum supported client</span></span> | <span data-ttu-id="dffd8-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="dffd8-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="dffd8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dffd8-121">Minimum supported server</span></span> | <span data-ttu-id="dffd8-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="dffd8-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="dffd8-123">Header</span><span class="sxs-lookup"><span data-stu-id="dffd8-123">Header</span></span>                   | <span data-ttu-id="dffd8-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="dffd8-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="dffd8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dffd8-125">Library</span></span>                  | <span data-ttu-id="dffd8-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="dffd8-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="dffd8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dffd8-127">Related topics</span></span>

* [<span data-ttu-id="dffd8-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="dffd8-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




