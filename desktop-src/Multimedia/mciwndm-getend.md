---
title: Сообщение MCIWNDM_GETEND (VFW. h)
description: Сообщение МЦИВНДМ \_ жетенд извлекает расположение конца содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетенд.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892577"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="825ee-105">\_Сообщение мЦивндм жетенд</span><span class="sxs-lookup"><span data-stu-id="825ee-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="825ee-106">Сообщение **мЦивндм \_ жетенд** извлекает расположение конца содержимого устройства или файла MCI.</span><span class="sxs-lookup"><span data-stu-id="825ee-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="825ee-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="825ee-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="825ee-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="825ee-108">Return Value</span></span>

<span data-ttu-id="825ee-109">Возвращает расположение в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="825ee-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="825ee-110">Требования</span><span class="sxs-lookup"><span data-stu-id="825ee-110">Requirements</span></span>



| <span data-ttu-id="825ee-111">Требование</span><span class="sxs-lookup"><span data-stu-id="825ee-111">Requirement</span></span> | <span data-ttu-id="825ee-112">Значение</span><span class="sxs-lookup"><span data-stu-id="825ee-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="825ee-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="825ee-113">Minimum supported client</span></span><br/> | <span data-ttu-id="825ee-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="825ee-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="825ee-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="825ee-115">Minimum supported server</span></span><br/> | <span data-ttu-id="825ee-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="825ee-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="825ee-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="825ee-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="825ee-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="825ee-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="825ee-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="825ee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825ee-120">**мЦивнджетенд**</span><span class="sxs-lookup"><span data-stu-id="825ee-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





