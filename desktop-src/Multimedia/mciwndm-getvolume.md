---
title: Сообщение MCIWNDM_GETVOLUME (VFW. h)
description: Сообщение МЦИВНДМ \_ . Volume получает текущую настройку тома для устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетволуме.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416069"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="d652b-105">\_Сообщение мЦивндм</span><span class="sxs-lookup"><span data-stu-id="d652b-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="d652b-106">Сообщение **мЦивндм. \_ Volume** получает текущую настройку тома для устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="d652b-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="d652b-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="d652b-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d652b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d652b-108">Return Value</span></span>

<span data-ttu-id="d652b-109">Возвращает текущий параметр тома.</span><span class="sxs-lookup"><span data-stu-id="d652b-109">Returns the current volume setting.</span></span> <span data-ttu-id="d652b-110">Значение по умолчанию ― 1000.</span><span class="sxs-lookup"><span data-stu-id="d652b-110">The default value is 1000.</span></span> <span data-ttu-id="d652b-111">Более высокие значения указывают громкости, а низкие значения указывают на незвуковые тома.</span><span class="sxs-lookup"><span data-stu-id="d652b-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d652b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d652b-112">Requirements</span></span>



| <span data-ttu-id="d652b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d652b-113">Requirement</span></span> | <span data-ttu-id="d652b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d652b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d652b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d652b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d652b-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d652b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d652b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d652b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d652b-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d652b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d652b-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d652b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d652b-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d652b-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d652b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d652b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d652b-122">**мЦивнджетволуме**</span><span class="sxs-lookup"><span data-stu-id="d652b-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





