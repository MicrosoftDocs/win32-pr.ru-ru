---
title: Сообщение MCIWNDM_CAN_EJECT (VFW. h)
description: МЦИВНДМ \_ может \_ извлечь сообщение, определяет, может ли устройство MCI извлечь свой носитель. Это сообщение можно отправить явно или с помощью макроса МЦивндканежект.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803916"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="165ba-105">МЦИВНДМ \_ может \_ извлечь сообщение</span><span class="sxs-lookup"><span data-stu-id="165ba-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="165ba-106">**МЦивндм \_ может \_ извлечь** сообщение, определяет, может ли устройство MCI извлечь свой носитель.</span><span class="sxs-lookup"><span data-stu-id="165ba-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="165ba-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндканежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .</span><span class="sxs-lookup"><span data-stu-id="165ba-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="165ba-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="165ba-108">Return Value</span></span>

<span data-ttu-id="165ba-109">Возвращает **значение true** , если устройство может извлечь носитель или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="165ba-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="165ba-110">Требования</span><span class="sxs-lookup"><span data-stu-id="165ba-110">Requirements</span></span>



| <span data-ttu-id="165ba-111">Требование</span><span class="sxs-lookup"><span data-stu-id="165ba-111">Requirement</span></span> | <span data-ttu-id="165ba-112">Значение</span><span class="sxs-lookup"><span data-stu-id="165ba-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="165ba-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="165ba-113">Minimum supported client</span></span><br/> | <span data-ttu-id="165ba-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="165ba-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="165ba-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="165ba-115">Minimum supported server</span></span><br/> | <span data-ttu-id="165ba-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="165ba-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="165ba-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="165ba-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="165ba-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="165ba-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165ba-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="165ba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165ba-120">**мЦивндканежект**</span><span class="sxs-lookup"><span data-stu-id="165ba-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





