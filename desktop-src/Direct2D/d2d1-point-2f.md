---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Представляет пару координат x и y в двухмерном пространстве. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674615"
---
# <a name="d2d1_point_2f"></a><span data-ttu-id="fdcf4-105">D2D1 \_ точка \_ 2F</span><span class="sxs-lookup"><span data-stu-id="fdcf4-105">D2D1\_POINT\_2F</span></span>

<span data-ttu-id="fdcf4-106">Представляет пару координат x и y в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="fdcf4-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a><span data-ttu-id="fdcf4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdcf4-107">Remarks</span></span>

<span data-ttu-id="fdcf4-108">Точки в Direct2D представлены структурами **D2D1 Point \_ \_ 2F** или [**D2D1 \_ Point \_ 2U**](d2d1-point-2u.md) .</span><span class="sxs-lookup"><span data-stu-id="fdcf4-108">Points in Direct2D are represented by the **D2D1\_POINT\_2F** or [**D2D1\_POINT\_2U**](d2d1-point-2u.md) structures.</span></span> <span data-ttu-id="fdcf4-109">Оба содержат пару координат x и y в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="fdcf4-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="fdcf4-110">Структура **D2D1 \_ точки \_ 2F** сохраняет координаты как значения **float** , а структура **\_ \_ типоразмера 2U в D2D1 Point** сохраняет их как значения **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="fdcf4-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="fdcf4-111">**D2D1 \_ ТОЧКА \_ 2F** — это новое имя для уже определенного типа с [**точкой постоянного тока \_ \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span><span class="sxs-lookup"><span data-stu-id="fdcf4-111">**D2D1\_POINT\_2F** is a new name for the already defined type [**D2D\_POINT\_2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdcf4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fdcf4-112">Requirements</span></span>



| <span data-ttu-id="fdcf4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fdcf4-113">Requirement</span></span> | <span data-ttu-id="fdcf4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fdcf4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdcf4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdcf4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fdcf4-116">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdcf4-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fdcf4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdcf4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fdcf4-118">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdcf4-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fdcf4-119">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="fdcf4-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="fdcf4-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdcf4-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="fdcf4-121">Header</span><span class="sxs-lookup"><span data-stu-id="fdcf4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdcf4-122"><dt>D2DBaseTypes. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf4-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fdcf4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdcf4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdcf4-124">**D2D1 \_ точка \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="fdcf4-124">**D2D1\_POINT\_2U**</span></span>](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[<span data-ttu-id="fdcf4-125">**\_Точка D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="fdcf4-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

