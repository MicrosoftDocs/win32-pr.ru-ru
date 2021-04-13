---
title: Сообщение MCIWNDM_GETSTART (VFW. h)
description: Сообщение МЦИВНДМ \_ OnStart получает расположение начала содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетстарт.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489417"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="096c3-105">Сообщение МЦИВНДМ о \_ запуске</span><span class="sxs-lookup"><span data-stu-id="096c3-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="096c3-106">Сообщение **мЦивндм \_ OnStart** получает расположение начала содержимого устройства или файла MCI.</span><span class="sxs-lookup"><span data-stu-id="096c3-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="096c3-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .</span><span class="sxs-lookup"><span data-stu-id="096c3-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="096c3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="096c3-108">Return Value</span></span>

<span data-ttu-id="096c3-109">Возвращает расположение в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="096c3-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="096c3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="096c3-110">Remarks</span></span>

<span data-ttu-id="096c3-111">Как правило, возвращаемое значение равно нулю; но некоторые устройства используют ненулевое начальное расположение.</span><span class="sxs-lookup"><span data-stu-id="096c3-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="096c3-112">При поиске в этом расположении устройство настраивается на начало носителя.</span><span class="sxs-lookup"><span data-stu-id="096c3-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="096c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="096c3-113">Requirements</span></span>



| <span data-ttu-id="096c3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="096c3-114">Requirement</span></span> | <span data-ttu-id="096c3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="096c3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="096c3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="096c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="096c3-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="096c3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="096c3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="096c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="096c3-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="096c3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="096c3-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="096c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="096c3-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="096c3-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="096c3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="096c3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096c3-123">**мЦивнджетстарт**</span><span class="sxs-lookup"><span data-stu-id="096c3-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





