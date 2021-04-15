---
title: Сообщение MCIWNDM_CAN_CONFIG (VFW. h)
description: Сообщение МЦИВНДМ \_ Can \_ config определяет, может ли устройство MCI отобразить диалоговое окно конфигурации. Это сообщение можно отправить явно или с помощью макроса МЦивндканконфиг.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493029"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="742a8-105">МЦИВНДМ \_ может \_ сообщение конфигурации</span><span class="sxs-lookup"><span data-stu-id="742a8-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="742a8-106">Сообщение **мЦивндм \_ Can \_ config** определяет, может ли устройство MCI отобразить диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="742a8-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="742a8-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндканконфиг**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .</span><span class="sxs-lookup"><span data-stu-id="742a8-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="742a8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="742a8-108">Return Value</span></span>

<span data-ttu-id="742a8-109">Возвращает **значение true** , если устройство поддерживает конфигурацию, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="742a8-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="742a8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="742a8-110">Requirements</span></span>



| <span data-ttu-id="742a8-111">Требование</span><span class="sxs-lookup"><span data-stu-id="742a8-111">Requirement</span></span> | <span data-ttu-id="742a8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="742a8-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="742a8-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="742a8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="742a8-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="742a8-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="742a8-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="742a8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="742a8-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="742a8-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="742a8-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="742a8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="742a8-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="742a8-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="742a8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="742a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742a8-120">**мЦивндканконфиг**</span><span class="sxs-lookup"><span data-stu-id="742a8-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





