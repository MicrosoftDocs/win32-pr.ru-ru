---
title: Сообщение MCIWNDM_CAN_SAVE (VFW. h)
description: МЦИВНДМ \_ может \_ сохранить сообщение, определяет, может ли устройство MCI сохранять данные. Это сообщение можно отправить явно или с помощью макроса МЦивндкансаве.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489573"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="aa5f5-105">МЦИВНДМ \_ может \_ сохранить сообщение</span><span class="sxs-lookup"><span data-stu-id="aa5f5-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="aa5f5-106">**МЦивндм \_ может \_ сохранить** сообщение, определяет, может ли устройство MCI сохранять данные.</span><span class="sxs-lookup"><span data-stu-id="aa5f5-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="aa5f5-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндкансаве**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .</span><span class="sxs-lookup"><span data-stu-id="aa5f5-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="aa5f5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa5f5-108">Return Value</span></span>

<span data-ttu-id="aa5f5-109">Возвращает **значение true** , если устройство поддерживает сохранение или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aa5f5-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5f5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="aa5f5-110">Requirements</span></span>



| <span data-ttu-id="aa5f5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="aa5f5-111">Requirement</span></span> | <span data-ttu-id="aa5f5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5f5-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aa5f5-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa5f5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5f5-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa5f5-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aa5f5-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa5f5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5f5-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa5f5-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aa5f5-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa5f5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5f5-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f5-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5f5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa5f5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5f5-120">**мЦивндкансаве**</span><span class="sxs-lookup"><span data-stu-id="aa5f5-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





