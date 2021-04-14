---
title: D2D1_TAG (D2d1. h)
description: Определяемое приложением 64-разрядное значение, используемое в параметре \ 160; пометить набор операций отрисовки.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340575"
---
# <a name="d2d1_tag"></a><span data-ttu-id="b191b-104">\_Тег D2D1</span><span class="sxs-lookup"><span data-stu-id="b191b-104">D2D1\_TAG</span></span>

<span data-ttu-id="b191b-105">Определяемое приложением 64-разрядное значение, используемое для пометки набора операций отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b191b-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="b191b-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b191b-106">Remarks</span></span>

<span data-ttu-id="b191b-107">Чтобы задать тег перед набором операций отрисовки, используйте метод [**ID2D1RenderTarget:: сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="b191b-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="b191b-108">Чтобы получить текущий тег, используйте метод [**ID2D1RenderTarget:: Tags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .</span><span class="sxs-lookup"><span data-stu-id="b191b-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b191b-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b191b-109">Requirements</span></span>



| <span data-ttu-id="b191b-110">Требование</span><span class="sxs-lookup"><span data-stu-id="b191b-110">Requirement</span></span> | <span data-ttu-id="b191b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b191b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b191b-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b191b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b191b-113">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="b191b-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b191b-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b191b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b191b-115">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b191b-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b191b-116">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="b191b-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b191b-117">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="b191b-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="b191b-118">Header</span><span class="sxs-lookup"><span data-stu-id="b191b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b191b-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="b191b-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="b191b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b191b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b191b-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="b191b-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="b191b-122">**сеттагс**</span><span class="sxs-lookup"><span data-stu-id="b191b-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

