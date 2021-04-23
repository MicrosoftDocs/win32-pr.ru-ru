---
title: Сообщение MCIWNDM_PLAYFROM (VFW. h)
description: Сообщение МЦИВНДМ \_ плайфром воспроизводит содержимое устройства mci из указанного расположения в конец содержимого или до тех пор, пока другая команда не останавливает воспроизведение. Это сообщение можно отправить явно или с помощью макроса МЦивндплайфром.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988307"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="038cb-105">\_Сообщение мЦивндм плайфром</span><span class="sxs-lookup"><span data-stu-id="038cb-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="038cb-106">Сообщение **мЦивндм \_ плайфром** ВОСПРОИЗВОДИТ содержимое устройства mci из указанного расположения в конец содержимого или до тех пор, пока другая команда не останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="038cb-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="038cb-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="038cb-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="038cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="038cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038cb-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*лпос*</span><span class="sxs-lookup"><span data-stu-id="038cb-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="038cb-110">Начальное расположение.</span><span class="sxs-lookup"><span data-stu-id="038cb-110">Starting location.</span></span> <span data-ttu-id="038cb-111">Единицы начального расположения зависят от текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="038cb-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038cb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="038cb-112">Return Value</span></span>

<span data-ttu-id="038cb-113">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="038cb-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="038cb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="038cb-114">Remarks</span></span>

<span data-ttu-id="038cb-115">Можно также указать начальное и конечное расположение для воспроизведения с помощью макроса [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="038cb-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="038cb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="038cb-116">Requirements</span></span>



| <span data-ttu-id="038cb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="038cb-117">Requirement</span></span> | <span data-ttu-id="038cb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="038cb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="038cb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="038cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="038cb-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="038cb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="038cb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="038cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="038cb-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="038cb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="038cb-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="038cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="038cb-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038cb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="038cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038cb-126">**мЦивндплайфром**</span><span class="sxs-lookup"><span data-stu-id="038cb-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="038cb-127">**мЦивндплайфромто**</span><span class="sxs-lookup"><span data-stu-id="038cb-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





