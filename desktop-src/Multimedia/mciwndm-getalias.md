---
title: Сообщение MCIWNDM_GETALIAS (VFW. h)
description: Сообщение МЦИВНДМ \_ . alias извлекает псевдоним, используемый для открытия устройства MCI или файла с помощью функции mciSendString. Это сообщение можно отправить явно или с помощью макроса МЦивнджеталиас.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672498"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="2752a-105">Сообщение МЦИВНДМ. \_ псевдоним</span><span class="sxs-lookup"><span data-stu-id="2752a-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="2752a-106">Сообщение **мЦивндм. \_ Alias** извлекает псевдоним, используемый для открытия устройства MCI или файла с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2752a-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="2752a-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджеталиас**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="2752a-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2752a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2752a-108">Return Value</span></span>

<span data-ttu-id="2752a-109">Возвращает псевдоним устройства.</span><span class="sxs-lookup"><span data-stu-id="2752a-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="2752a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2752a-110">Requirements</span></span>



| <span data-ttu-id="2752a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2752a-111">Requirement</span></span> | <span data-ttu-id="2752a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2752a-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2752a-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2752a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2752a-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2752a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2752a-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2752a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2752a-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2752a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2752a-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2752a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2752a-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2752a-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2752a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2752a-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="2752a-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2752a-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2752a-121">**мЦивнджеталиас**</span><span class="sxs-lookup"><span data-stu-id="2752a-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

