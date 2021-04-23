---
title: Сообщение MCIWNDM_GET_DEST (VFW. h)
description: Сообщение МЦИВНДМ \_ Get \_ dest получает координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивнджетдест.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071091"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="61baa-105">МЦИВНДМ \_ Получение \_ сообщения о приемнике</span><span class="sxs-lookup"><span data-stu-id="61baa-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="61baa-106">Сообщение **мЦивндм \_ Get \_ dest** получает координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="61baa-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="61baa-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .</span><span class="sxs-lookup"><span data-stu-id="61baa-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="61baa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61baa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61baa-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="61baa-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="61baa-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , чтобы вернуть координаты прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="61baa-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61baa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61baa-111">Return Value</span></span>

<span data-ttu-id="61baa-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="61baa-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="61baa-113">Требования</span><span class="sxs-lookup"><span data-stu-id="61baa-113">Requirements</span></span>



| <span data-ttu-id="61baa-114">Требование</span><span class="sxs-lookup"><span data-stu-id="61baa-114">Requirement</span></span> | <span data-ttu-id="61baa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="61baa-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="61baa-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61baa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61baa-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61baa-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="61baa-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61baa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61baa-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61baa-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61baa-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61baa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61baa-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61baa-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61baa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61baa-123">**мЦивнджетдест**</span><span class="sxs-lookup"><span data-stu-id="61baa-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

