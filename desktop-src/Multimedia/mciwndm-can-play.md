---
title: Сообщение MCIWNDM_CAN_PLAY (VFW. h)
description: МЦИВНДМ \_ может \_ воспроизвести сообщение определяет, может ли устройство MCI воспроизвести файл данных или содержимое какого-либо другого типа. Это сообщение можно отправить явно или с помощью макроса МЦивндканплай.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672887"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="b268e-105">МЦИВНДМ \_ может \_ воспроизвести сообщение</span><span class="sxs-lookup"><span data-stu-id="b268e-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="b268e-106">**МЦивндм \_ может \_ воспроизвести** сообщение определяет, может ли устройство MCI воспроизвести файл данных или содержимое какого-либо другого типа.</span><span class="sxs-lookup"><span data-stu-id="b268e-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="b268e-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндканплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .</span><span class="sxs-lookup"><span data-stu-id="b268e-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b268e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b268e-108">Return Value</span></span>

<span data-ttu-id="b268e-109">Возвращает **значение true** , если устройство поддерживает воспроизведение данных, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b268e-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b268e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b268e-110">Requirements</span></span>



| <span data-ttu-id="b268e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b268e-111">Requirement</span></span> | <span data-ttu-id="b268e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b268e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b268e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b268e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b268e-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b268e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b268e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b268e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b268e-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b268e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b268e-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b268e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b268e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b268e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b268e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b268e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b268e-120">**мЦивндканплай**</span><span class="sxs-lookup"><span data-stu-id="b268e-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





