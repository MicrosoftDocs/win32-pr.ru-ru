---
title: Сообщение MCIWNDM_GETREPEAT (VFW. h)
description: Сообщение МЦИВНДМ \_ повторяемости определяет, активировано ли непрерывное воспроизведение. Это сообщение можно отправить явно или с помощью макроса МЦивнджетрепеат.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135283"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="c50b0-105">\_Сообщение МЦИВНДМ Repeat</span><span class="sxs-lookup"><span data-stu-id="c50b0-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="c50b0-106">Сообщение **МЦИВНДМ \_ повторяемости** определяет, активировано ли непрерывное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="c50b0-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="c50b0-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="c50b0-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c50b0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c50b0-108">Return Value</span></span>

<span data-ttu-id="c50b0-109">Возвращает **значение true** , если непрерывное воспроизведение активировано, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c50b0-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c50b0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c50b0-110">Requirements</span></span>



| <span data-ttu-id="c50b0-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c50b0-111">Requirement</span></span> | <span data-ttu-id="c50b0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c50b0-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c50b0-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c50b0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c50b0-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c50b0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c50b0-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c50b0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c50b0-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c50b0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c50b0-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c50b0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50b0-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50b0-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50b0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c50b0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50b0-120">**мЦивнджетрепеат**</span><span class="sxs-lookup"><span data-stu-id="c50b0-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





