---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Сохраняет упорядоченную пару с плавающей запятой, обычно ширину и высоту прямоугольника.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489759"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="3fce1-104">D2D1 \_ размер \_ F</span><span class="sxs-lookup"><span data-stu-id="3fce1-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="3fce1-105">Сохраняет упорядоченную пару с плавающей запятой, обычно ширину и высоту прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3fce1-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="3fce1-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fce1-106">Remarks</span></span>

<span data-ttu-id="3fce1-107">Как и точки, размеры являются еще одной важной концепцией графики.</span><span class="sxs-lookup"><span data-stu-id="3fce1-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="3fce1-108">В Direct2D размеры представлены структурами **D2D1 \_ size \_ F** или [**D2D1 \_ size \_ U**](d2d1-size-u.md) .</span><span class="sxs-lookup"><span data-stu-id="3fce1-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="3fce1-109">Оба содержат упорядоченную пару чисел, обычно ширину и высоту прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3fce1-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="3fce1-110">Структура **D2D1 \_ size \_ F** содержит упорядоченную пару значений **float** , а структура **D2D1 \_ size \_ U** содержит упорядоченную пару значений **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="3fce1-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="3fce1-111">**D2D1 \_ РАЗМЕР \_ f** — это новое имя для уже определенного типа **D2D, \_ равный \_ f**.</span><span class="sxs-lookup"><span data-stu-id="3fce1-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="3fce1-112">Список полей, предоставляемых **D2D1 \_ size \_ f**, см. в разделе **\_ Размер D2D \_ f**.</span><span class="sxs-lookup"><span data-stu-id="3fce1-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fce1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3fce1-113">Requirements</span></span>



| <span data-ttu-id="3fce1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3fce1-114">Requirement</span></span> | <span data-ttu-id="3fce1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3fce1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fce1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fce1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3fce1-117">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="3fce1-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3fce1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fce1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3fce1-119">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3fce1-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3fce1-120">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="3fce1-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="3fce1-121">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="3fce1-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="3fce1-122">Header</span><span class="sxs-lookup"><span data-stu-id="3fce1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fce1-123"><dt>D2DBaseTypes. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fce1-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3fce1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fce1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fce1-125">**\_Размер D2D \_ F**</span><span class="sxs-lookup"><span data-stu-id="3fce1-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="3fce1-126">**D2D1 \_ размер \_ U**</span><span class="sxs-lookup"><span data-stu-id="3fce1-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="3fce1-127">**D2D1 \_ точка \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="3fce1-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

