---
title: Сообщение MCIWNDM_CAN_WINDOW (VFW. h)
description: МЦИВНДМ \_ может \_ поwindow Message определяет, поддерживает ли устройство MCI команды MCI, ориентированные на окна. Это сообщение можно отправить явно или с помощью макроса МЦивндканвиндов.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988533"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="02565-105">МЦИВНДМ \_ может \_ пооконное сообщение</span><span class="sxs-lookup"><span data-stu-id="02565-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="02565-106">**МЦивндм \_ может \_ поwindow** Message определяет, поддерживает ли устройство MCI команды MCI, ориентированные на окна.</span><span class="sxs-lookup"><span data-stu-id="02565-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="02565-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндканвиндов**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .</span><span class="sxs-lookup"><span data-stu-id="02565-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="02565-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02565-108">Return Value</span></span>

<span data-ttu-id="02565-109">Возвращает **значение true** , если устройство поддерживает команды MCI, ориентированные на окна, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="02565-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="02565-110">Требования</span><span class="sxs-lookup"><span data-stu-id="02565-110">Requirements</span></span>



| <span data-ttu-id="02565-111">Требование</span><span class="sxs-lookup"><span data-stu-id="02565-111">Requirement</span></span> | <span data-ttu-id="02565-112">Значение</span><span class="sxs-lookup"><span data-stu-id="02565-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="02565-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02565-113">Minimum supported client</span></span><br/> | <span data-ttu-id="02565-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02565-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="02565-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02565-115">Minimum supported server</span></span><br/> | <span data-ttu-id="02565-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02565-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="02565-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="02565-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="02565-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="02565-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02565-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02565-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02565-120">**мЦивндканвиндов**</span><span class="sxs-lookup"><span data-stu-id="02565-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





