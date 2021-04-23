---
title: Сообщение MCIWNDM_SETREPEAT (VFW. h)
description: Сообщение МЦИВНДМ \_ сетрепеат устанавливает флаг повтора, связанный с непрерывным воспроизведением.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892265"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="ab535-104">\_Сообщение мЦивндм сетрепеат</span><span class="sxs-lookup"><span data-stu-id="ab535-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="ab535-105">Сообщение **мЦивндм \_ сетрепеат** устанавливает флаг повтора, связанный с непрерывным воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="ab535-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="ab535-106">Сообщение **мЦивндм \_ сетрепеат** работает совместно с командой [MCI \_ Play](mci-play.md) , чтобы обеспечить непрерывный цикл воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ab535-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="ab535-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="ab535-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="ab535-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab535-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab535-109"><span id="f"></span><span id="F"></span>*ж*</span><span class="sxs-lookup"><span data-stu-id="ab535-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="ab535-110">Новое состояние флага повтора.</span><span class="sxs-lookup"><span data-stu-id="ab535-110">New state of the repeat flag.</span></span> <span data-ttu-id="ab535-111">Укажите **значение true** , чтобы включить непрерывное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="ab535-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab535-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab535-112">Return Value</span></span>

<span data-ttu-id="ab535-113">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ab535-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab535-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab535-114">Remarks</span></span>

<span data-ttu-id="ab535-115">В настоящее время МЦИАВИ является единственным устройством, поддерживающим непрерывное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="ab535-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab535-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ab535-116">Requirements</span></span>



| <span data-ttu-id="ab535-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ab535-117">Requirement</span></span> | <span data-ttu-id="ab535-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ab535-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab535-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab535-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab535-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ab535-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab535-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab535-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab535-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ab535-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab535-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ab535-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab535-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab535-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab535-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab535-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab535-126">\_Воспроизведение MCI</span><span class="sxs-lookup"><span data-stu-id="ab535-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="ab535-127">**мЦивндсетрепеат**</span><span class="sxs-lookup"><span data-stu-id="ab535-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





