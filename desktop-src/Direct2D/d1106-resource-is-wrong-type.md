---
title: Недопустимый тип ресурса D1106
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: Данный ресурс имеет тип, отличный от ожидаемого.
keywords:
- Недопустимый тип ресурса D1106 Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649145"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="28297-104">D1106: недопустимый тип ресурса</span><span class="sxs-lookup"><span data-stu-id="28297-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="28297-105">Указанный ресурс ресурса \[  \] не имеет ожидаемого типа.</span><span class="sxs-lookup"><span data-stu-id="28297-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="28297-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="28297-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="28297-107"><span id="resource"></span><span id="RESOURCE"></span>*ресурсов*</span><span class="sxs-lookup"><span data-stu-id="28297-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="28297-108">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="28297-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="28297-109">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="28297-109">Possible Causes</span></span>

<span data-ttu-id="28297-110">Интерфейс был неправильно приведен и использован в качестве параметра для метода или функции.</span><span class="sxs-lookup"><span data-stu-id="28297-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="28297-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="28297-111">Examples</span></span>

<span data-ttu-id="28297-112">В следующем примере объект [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) передается, когда ожидается [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="28297-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="28297-113">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="28297-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="28297-114">Исправления</span><span class="sxs-lookup"><span data-stu-id="28297-114">Fixes</span></span>

<span data-ttu-id="28297-115">Используйте тип, требуемый для метода.</span><span class="sxs-lookup"><span data-stu-id="28297-115">Use the type required by the method.</span></span>

 

 
