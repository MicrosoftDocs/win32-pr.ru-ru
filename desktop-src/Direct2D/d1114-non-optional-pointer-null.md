---
title: D1114 не Необязательный указатель NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Параметр интерфейса:: method является необязательным. Передан пустой указатель. Это приведет к сбою Direct2D.'
keywords:
- D1114 Необязательный указатель NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649143"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="6aa8e-106">D1114: Необязательный указатель NULL</span><span class="sxs-lookup"><span data-stu-id="6aa8e-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="6aa8e-107">Параметр параметра \[  \] *интерфейса*::*method* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="6aa8e-108">Передан **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="6aa8e-109">Это приведет к сбою Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="6aa8e-110">Заполнители</span><span class="sxs-lookup"><span data-stu-id="6aa8e-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="6aa8e-111"><span id="parameter"></span><span id="PARAMETER"></span>*параметр*</span><span class="sxs-lookup"><span data-stu-id="6aa8e-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="6aa8e-112">Имя параметра, содержащего указатель **null** .</span><span class="sxs-lookup"><span data-stu-id="6aa8e-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="6aa8e-113"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="6aa8e-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="6aa8e-114">Имя интерфейса, которому принадлежит *метод* .</span><span class="sxs-lookup"><span data-stu-id="6aa8e-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="6aa8e-115"><span id="method"></span><span id="METHOD"></span>*Method*</span><span class="sxs-lookup"><span data-stu-id="6aa8e-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="6aa8e-116">Имя метода, получившего недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="6aa8e-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="6aa8e-117">Examples</span></span>

<span data-ttu-id="6aa8e-118">В следующем примере показано, что метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) получает указатель null для необязательного параметра *Geometry* .</span><span class="sxs-lookup"><span data-stu-id="6aa8e-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="6aa8e-119">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="6aa8e-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="6aa8e-120">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="6aa8e-120">Possible Causes</span></span>

<span data-ttu-id="6aa8e-121">Для необязательного параметра был передан пустой указатель.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="6aa8e-122">Исправления</span><span class="sxs-lookup"><span data-stu-id="6aa8e-122">Fixes</span></span>

<span data-ttu-id="6aa8e-123">Убедитесь, что необязательный параметр не имеет ПУСТого указателя.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 
