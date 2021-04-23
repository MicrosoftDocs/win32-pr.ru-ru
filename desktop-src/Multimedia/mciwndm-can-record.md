---
title: Сообщение MCIWNDM_CAN_RECORD (VFW. h)
description: МЦИВНДМ \_ может \_ записывать сообщение, определяет, поддерживает ли устройство MCI запись. Это сообщение можно отправить явно или с помощью макроса МЦивндканрекорд.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492612"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="5393e-105">МЦИВНДМ \_ может \_ записать сообщение</span><span class="sxs-lookup"><span data-stu-id="5393e-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="5393e-106">**МЦивндм \_ может \_ записывать** сообщение, определяет, поддерживает ли устройство MCI запись.</span><span class="sxs-lookup"><span data-stu-id="5393e-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="5393e-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндканрекорд**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .</span><span class="sxs-lookup"><span data-stu-id="5393e-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5393e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5393e-108">Return Value</span></span>

<span data-ttu-id="5393e-109">Возвращает **значение true** , если устройство поддерживает запись или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5393e-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5393e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="5393e-110">Requirements</span></span>



| <span data-ttu-id="5393e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="5393e-111">Requirement</span></span> | <span data-ttu-id="5393e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5393e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5393e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5393e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5393e-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5393e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5393e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5393e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5393e-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5393e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5393e-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5393e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5393e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5393e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5393e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5393e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5393e-120">**мЦивндканрекорд**</span><span class="sxs-lookup"><span data-stu-id="5393e-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





