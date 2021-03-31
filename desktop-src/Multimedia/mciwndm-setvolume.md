---
title: Сообщение MCIWNDM_SETVOLUME (VFW. h)
description: В \_ сообщении мЦивндм сетволуме задается уровень громкости устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивндсетволуме.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801324"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="3f368-105">\_Сообщение мЦивндм сетволуме</span><span class="sxs-lookup"><span data-stu-id="3f368-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="3f368-106">В сообщении **мЦивндм \_ сетволуме** задается уровень громкости устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="3f368-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="3f368-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="3f368-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="3f368-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f368-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f368-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*ивол*</span><span class="sxs-lookup"><span data-stu-id="3f368-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="3f368-110">Новый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="3f368-110">New volume level.</span></span> <span data-ttu-id="3f368-111">Укажите 1000 для обычного уровня громкости.</span><span class="sxs-lookup"><span data-stu-id="3f368-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="3f368-112">Укажите более высокое значение громкости или более низкое значение для звукового тома.</span><span class="sxs-lookup"><span data-stu-id="3f368-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f368-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f368-113">Return Value</span></span>

<span data-ttu-id="3f368-114">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f368-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f368-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3f368-115">Requirements</span></span>



| <span data-ttu-id="3f368-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3f368-116">Requirement</span></span> | <span data-ttu-id="3f368-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3f368-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3f368-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f368-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f368-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f368-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3f368-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f368-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f368-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f368-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f368-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f368-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f368-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f368-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f368-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f368-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f368-125">**мЦивндсетволуме**</span><span class="sxs-lookup"><span data-stu-id="3f368-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





