---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Представляет пару координат x и y в двухмерном пространстве. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273504"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="ef27f-105">D2D1 \_ точка \_ 2U</span><span class="sxs-lookup"><span data-stu-id="ef27f-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="ef27f-106">Представляет пару координат x и y в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="ef27f-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="ef27f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef27f-107">Remarks</span></span>

<span data-ttu-id="ef27f-108">Точки в Direct2D представлены структурами [**D2D1 Point \_ \_ 2F**](d2d1-point-2f.md) или **D2D1 \_ Point \_ 2U** .</span><span class="sxs-lookup"><span data-stu-id="ef27f-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="ef27f-109">Оба содержат пару координат x и y в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="ef27f-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="ef27f-110">Структура **D2D1 \_ точки \_ 2F** сохраняет координаты как значения **float** , а структура **\_ \_ типоразмера 2U в D2D1 Point** сохраняет их как значения **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="ef27f-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="ef27f-111">**D2D1 \_ ТОЧКА \_ 2U** — это новое имя уже определенного типа для [**точки D2D с типом \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="ef27f-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef27f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ef27f-112">Requirements</span></span>



| <span data-ttu-id="ef27f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ef27f-113">Requirement</span></span> | <span data-ttu-id="ef27f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ef27f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef27f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef27f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ef27f-116">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="ef27f-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="ef27f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef27f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ef27f-118">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ef27f-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ef27f-119">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="ef27f-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ef27f-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef27f-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="ef27f-121">Header</span><span class="sxs-lookup"><span data-stu-id="ef27f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef27f-122"><dt>D2DBaseTypes. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef27f-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ef27f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef27f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef27f-124">**Точка D2D с \_ \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="ef27f-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="ef27f-125">**\_Точка D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="ef27f-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





