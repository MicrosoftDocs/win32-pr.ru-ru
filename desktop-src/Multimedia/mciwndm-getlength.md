---
title: Сообщение MCIWNDM_GETLENGTH (VFW. h)
description: Сообщение МЦИВНДМ \_ DATALENGTH извлекает длину содержимого или файла, который в настоящее время используется устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетленгс.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489420"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="ed093-105">Сообщение МЦИВНДМ о \_ длительности</span><span class="sxs-lookup"><span data-stu-id="ed093-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="ed093-106">Сообщение **МЦИВНДМ \_ DATALENGTH** извлекает длину содержимого или файла, который в настоящее время используется устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="ed093-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="ed093-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетленгс**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="ed093-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ed093-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed093-108">Return Value</span></span>

<span data-ttu-id="ed093-109">Возвращает длину.</span><span class="sxs-lookup"><span data-stu-id="ed093-109">Returns the length.</span></span> <span data-ttu-id="ed093-110">Единицы длины зависят от текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="ed093-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed093-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ed093-111">Requirements</span></span>



| <span data-ttu-id="ed093-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ed093-112">Requirement</span></span> | <span data-ttu-id="ed093-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ed093-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed093-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed093-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ed093-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed093-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed093-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed093-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ed093-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed093-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed093-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ed093-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed093-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed093-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed093-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed093-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed093-121">**мЦивнджетленгс**</span><span class="sxs-lookup"><span data-stu-id="ed093-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





