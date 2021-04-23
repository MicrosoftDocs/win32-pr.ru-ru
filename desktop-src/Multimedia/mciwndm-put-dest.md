---
title: Сообщение MCIWNDM_PUT_DEST (VFW. h)
description: '\_Сообщение о мЦивндме размещения \_ переопределяет координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивндпутдест.'
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803364"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="6c3ec-105">МЦИВНДМ \_ Размещение \_ сообщения о приемнике</span><span class="sxs-lookup"><span data-stu-id="6c3ec-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="6c3ec-106">Сообщение о **мЦивндме \_ размещения \_** переопределяет координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6c3ec-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="6c3ec-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндпутдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="6c3ec-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="6c3ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c3ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3ec-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="6c3ec-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="6c3ec-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="6c3ec-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3ec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c3ec-111">Return Value</span></span>

<span data-ttu-id="6c3ec-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c3ec-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3ec-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3ec-113">Requirements</span></span>



| <span data-ttu-id="6c3ec-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6c3ec-114">Requirement</span></span> | <span data-ttu-id="6c3ec-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c3ec-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c3ec-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c3ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3ec-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c3ec-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c3ec-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c3ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3ec-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c3ec-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c3ec-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6c3ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3ec-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ec-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c3ec-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c3ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ec-123">**мЦивндпутдест**</span><span class="sxs-lookup"><span data-stu-id="6c3ec-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

