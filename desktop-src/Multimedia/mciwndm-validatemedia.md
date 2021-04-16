---
title: Сообщение MCIWNDM_VALIDATEMEDIA (VFW. h)
description: Сообщение МЦИВНДМ \_ валидатемедиа обновляет начальные и конечные расположения содержимого, текущую положение в содержимом и значение TrackBar в соответствии с текущим форматом времени.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533797"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="b7e77-104">\_Сообщение мЦивндм валидатемедиа</span><span class="sxs-lookup"><span data-stu-id="b7e77-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="b7e77-105">Сообщение **мЦивндм \_ валидатемедиа** обновляет начальные и конечные расположения содержимого, текущую положение в содержимом и значение TrackBar в соответствии с текущим форматом времени.</span><span class="sxs-lookup"><span data-stu-id="b7e77-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="b7e77-106">Это сообщение можно отправить явно или с помощью макроса [**мЦивндвалидатемедиа**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .</span><span class="sxs-lookup"><span data-stu-id="b7e77-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b7e77-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7e77-107">Return Value</span></span>

<span data-ttu-id="b7e77-108">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b7e77-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e77-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7e77-109">Remarks</span></span>

<span data-ttu-id="b7e77-110">Как правило, использовать этот макрос не требуется. Однако, если приложение изменяет формат времени устройства без использования МЦивнд; начальное и конечное расположение содержимого, а также значение TrackBar, продолжайте использовать старый формат.</span><span class="sxs-lookup"><span data-stu-id="b7e77-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="b7e77-111">Этот макрос можно использовать для обновления этих значений.</span><span class="sxs-lookup"><span data-stu-id="b7e77-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e77-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b7e77-112">Requirements</span></span>



| <span data-ttu-id="b7e77-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b7e77-113">Requirement</span></span> | <span data-ttu-id="b7e77-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b7e77-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7e77-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7e77-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e77-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7e77-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b7e77-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7e77-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e77-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7e77-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b7e77-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b7e77-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e77-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e77-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e77-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7e77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e77-122">**мЦивндвалидатемедиа**</span><span class="sxs-lookup"><span data-stu-id="b7e77-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





