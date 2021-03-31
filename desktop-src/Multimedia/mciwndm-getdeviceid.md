---
title: Сообщение MCIWNDM_GETDEVICEID (VFW. h)
description: Сообщение МЦИВНДМ \_ GETDEVICEID получает идентификатор открытого устройства MCI для использования с функцией мЦисендкомманд. Это сообщение можно отправить явно или с помощью макроса МЦивнджетдевицеид.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071233"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="e8010-105">\_Сообщение мЦивндм GETDEVICEID</span><span class="sxs-lookup"><span data-stu-id="e8010-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="e8010-106">Сообщение **мЦивндм \_ GETDEVICEID** получает идентификатор открытого устройства MCI для использования с функцией [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e8010-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="e8010-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетдевицеид**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="e8010-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e8010-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8010-108">Return Value</span></span>

<span data-ttu-id="e8010-109">Возвращает идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="e8010-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8010-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e8010-110">Requirements</span></span>



| <span data-ttu-id="e8010-111">Требование</span><span class="sxs-lookup"><span data-stu-id="e8010-111">Requirement</span></span> | <span data-ttu-id="e8010-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e8010-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e8010-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8010-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e8010-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8010-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e8010-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8010-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e8010-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8010-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e8010-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8010-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8010-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8010-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8010-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8010-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8010-120">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8010-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e8010-121">**мЦивнджетдевицеид**</span><span class="sxs-lookup"><span data-stu-id="e8010-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

