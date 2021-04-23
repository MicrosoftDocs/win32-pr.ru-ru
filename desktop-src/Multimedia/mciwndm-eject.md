---
title: Сообщение MCIWNDM_EJECT (VFW. h)
description: Сообщение о \_ извлечении мЦивндм отправляет команду на устройство MCI для извлечения носителя. Это сообщение можно отправить явно или с помощью макроса МЦивндежект.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414997"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="acaef-105">\_Сообщение о извлечении мЦивндм</span><span class="sxs-lookup"><span data-stu-id="acaef-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="acaef-106">Сообщение **о \_ извлечении мЦивндм** отправляет команду на устройство MCI для извлечения носителя.</span><span class="sxs-lookup"><span data-stu-id="acaef-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="acaef-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .</span><span class="sxs-lookup"><span data-stu-id="acaef-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="acaef-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acaef-108">Return Value</span></span>

<span data-ttu-id="acaef-109">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="acaef-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="acaef-110">Требования</span><span class="sxs-lookup"><span data-stu-id="acaef-110">Requirements</span></span>



| <span data-ttu-id="acaef-111">Требование</span><span class="sxs-lookup"><span data-stu-id="acaef-111">Requirement</span></span> | <span data-ttu-id="acaef-112">Значение</span><span class="sxs-lookup"><span data-stu-id="acaef-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="acaef-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acaef-113">Minimum supported client</span></span><br/> | <span data-ttu-id="acaef-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acaef-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="acaef-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acaef-115">Minimum supported server</span></span><br/> | <span data-ttu-id="acaef-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acaef-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="acaef-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="acaef-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="acaef-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="acaef-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acaef-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acaef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acaef-120">**мЦивндежект**</span><span class="sxs-lookup"><span data-stu-id="acaef-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





