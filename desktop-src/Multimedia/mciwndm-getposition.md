---
title: Сообщение MCIWNDM_GETPOSITION (VFW. h)
description: Сообщение МЦИВНДМ \_ Disposition извлекает числовое значение текущей позицией в содержимом устройства MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891545"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="d0817-104">\_Сообщение мЦивндм</span><span class="sxs-lookup"><span data-stu-id="d0817-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="d0817-105">Сообщение **МЦИВНДМ \_ Disposition** извлекает числовое значение текущей позицией в содержимом устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="d0817-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="d0817-106">Этот макрос также предоставляет текущую точку в виде строки в определяемом приложением буфере.</span><span class="sxs-lookup"><span data-stu-id="d0817-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="d0817-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетпоситион**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) или [**мЦивнджетпоситионстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="d0817-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="d0817-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0817-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0817-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="d0817-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="d0817-110">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="d0817-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="d0817-111">Если строка, завершающаяся нулем, длиннее, чем буфер, она усекается.</span><span class="sxs-lookup"><span data-stu-id="d0817-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="d0817-112">Используйте ноль, чтобы запретить получение позиций в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d0817-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="d0817-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="d0817-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="d0817-114">Указатель на определенный приложением буфер, используемый для возврата позиции.</span><span class="sxs-lookup"><span data-stu-id="d0817-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="d0817-115">Используйте ноль, чтобы запретить получение позиций в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d0817-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="d0817-116">Если устройство поддерживает записи, сведения о положении строки возвращаются в формате TT: MM: SS: FF, где TT соответствует дорожкам, MM и SS соответствуют минутам и секундам, а FF соответствует кадрам.</span><span class="sxs-lookup"><span data-stu-id="d0817-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0817-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0817-117">Return Value</span></span>

<span data-ttu-id="d0817-118">Возвращает целое число, соответствующее текущему положению.</span><span class="sxs-lookup"><span data-stu-id="d0817-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="d0817-119">Единицы для значения «значение» зависят от текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="d0817-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0817-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d0817-120">Requirements</span></span>



| <span data-ttu-id="d0817-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d0817-121">Requirement</span></span> | <span data-ttu-id="d0817-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d0817-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d0817-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0817-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0817-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0817-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d0817-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0817-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0817-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0817-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0817-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0817-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0817-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0817-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0817-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0817-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0817-130">**мЦивнджетпоситион**</span><span class="sxs-lookup"><span data-stu-id="d0817-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="d0817-131">**мЦивнджетпоситионстринг**</span><span class="sxs-lookup"><span data-stu-id="d0817-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





