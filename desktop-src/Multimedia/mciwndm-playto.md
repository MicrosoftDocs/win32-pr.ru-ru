---
title: Сообщение MCIWNDM_PLAYTO (VFW. h)
description: Сообщение МЦИВНДМ \_ плайто воспроизводит содержимое устройства mci из текущей позиции в указанное конечное расположение или до тех пор, пока другая команда не останавливает воспроизведение.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137066"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="6c2e0-104">\_Сообщение мЦивндм плайто</span><span class="sxs-lookup"><span data-stu-id="6c2e0-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="6c2e0-105">Сообщение **мЦивндм \_ плайто** ВОСПРОИЗВОДИТ содержимое устройства mci из текущей позиции в указанное конечное расположение или до тех пор, пока другая команда не останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="6c2e0-106">Если указанное конечное расположение находится за пределами конца содержимого, воспроизведение останавливается в конце содержимого.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="6c2e0-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="6c2e0-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="6c2e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c2e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2e0-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Пользование*</span><span class="sxs-lookup"><span data-stu-id="6c2e0-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="6c2e0-110">Конечное расположение.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-110">Ending location.</span></span> <span data-ttu-id="6c2e0-111">Единицы для конечного расположения зависят от текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2e0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c2e0-112">Return Value</span></span>

<span data-ttu-id="6c2e0-113">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2e0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c2e0-114">Remarks</span></span>

<span data-ttu-id="6c2e0-115">Этот макрос определяется с помощью макросов [**мЦивндсик**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) и [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , который, в свою очередь, использует команду [MCI \_ Seek](mci-seek.md) и сообщение **мЦивндм \_ плайто** .</span><span class="sxs-lookup"><span data-stu-id="6c2e0-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="6c2e0-116">Можно также указать начальное и конечное расположение для воспроизведения с помощью макроса [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="6c2e0-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2e0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6c2e0-117">Requirements</span></span>



| <span data-ttu-id="6c2e0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6c2e0-118">Requirement</span></span> | <span data-ttu-id="6c2e0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6c2e0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c2e0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c2e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2e0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c2e0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c2e0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c2e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2e0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c2e0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c2e0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6c2e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c2e0-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c2e0-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2e0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c2e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2e0-127">\_Поиск MCI</span><span class="sxs-lookup"><span data-stu-id="6c2e0-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="6c2e0-128">**мЦивндплайфромто**</span><span class="sxs-lookup"><span data-stu-id="6c2e0-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="6c2e0-129">**мЦивндплайто**</span><span class="sxs-lookup"><span data-stu-id="6c2e0-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="6c2e0-130">**мЦивндсик**</span><span class="sxs-lookup"><span data-stu-id="6c2e0-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





