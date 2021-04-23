---
title: ID2D1SolidColorBrush Сетколор методы
description: Задает цвет сплошной кисти цвета.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Методы Сетколор Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679657"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="55573-104">Методы ID2D1SolidColorBrush:: Сетколор</span><span class="sxs-lookup"><span data-stu-id="55573-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="55573-105">Задает цвет сплошной кисти цвета.</span><span class="sxs-lookup"><span data-stu-id="55573-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="55573-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="55573-106">Overload list</span></span>



| <span data-ttu-id="55573-107">Метод</span><span class="sxs-lookup"><span data-stu-id="55573-107">Method</span></span>                                                                          | <span data-ttu-id="55573-108">Описание</span><span class="sxs-lookup"><span data-stu-id="55573-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="55573-109">[**Сетколор (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="55573-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="55573-110">Задает цвет кисти с сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="55573-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="55573-111">[**Сетколор (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="55573-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="55573-112">Задает цвет сплошной кисти цвета.</span><span class="sxs-lookup"><span data-stu-id="55573-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="55573-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55573-113">Remarks</span></span>

<span data-ttu-id="55573-114">Чтобы облегчить создание цветов, Direct2D предоставляет класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="55573-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="55573-115">Он предлагает несколько вспомогательных методов для создания цветов и предоставляет набор или стандартные цвета.</span><span class="sxs-lookup"><span data-stu-id="55573-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="55573-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="55573-116">Examples</span></span>

<span data-ttu-id="55573-117">В следующем коде показано, как использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="55573-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="55573-118">Требования</span><span class="sxs-lookup"><span data-stu-id="55573-118">Requirements</span></span>



| <span data-ttu-id="55573-119">Требование</span><span class="sxs-lookup"><span data-stu-id="55573-119">Requirement</span></span> | <span data-ttu-id="55573-120">Значение</span><span class="sxs-lookup"><span data-stu-id="55573-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55573-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55573-121">Library</span></span><br/> | <dl> <span data-ttu-id="55573-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55573-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="55573-123">DLL</span><span class="sxs-lookup"><span data-stu-id="55573-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="55573-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55573-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55573-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55573-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55573-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="55573-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

