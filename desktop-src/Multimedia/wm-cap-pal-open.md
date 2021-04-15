---
title: Сообщение WM_CAP_PAL_OPEN (VFW. h)
description: Сообщение WM \_ Cap \_ PAL \_ Open загружает новую палитру из файла палитры и передает его драйверу записи.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661835"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="b6f11-104">\_ \_ Открытое сообщение с ограничением WM PAL \_</span><span class="sxs-lookup"><span data-stu-id="b6f11-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="b6f11-105">Сообщение **WM \_ Cap \_ PAL \_ Open** загружает новую палитру из файла палитры и передает его драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="b6f11-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="b6f11-106">Файлы палитры обычно используют расширение имени файла. Списком.</span><span class="sxs-lookup"><span data-stu-id="b6f11-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="b6f11-107">Драйвер записи использует палитру, если это требуется для указанного формата изображения в цифровом формате.</span><span class="sxs-lookup"><span data-stu-id="b6f11-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="b6f11-108">Это сообщение можно отправить явно или с помощью макроса [**каппалеттеопен**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .</span><span class="sxs-lookup"><span data-stu-id="b6f11-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="b6f11-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6f11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f11-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="b6f11-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="b6f11-111">Указатель на строку с завершающим нулем, содержащую имя файла палитры.</span><span class="sxs-lookup"><span data-stu-id="b6f11-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f11-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6f11-112">Return Value</span></span>

<span data-ttu-id="b6f11-113">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b6f11-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="b6f11-114">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="b6f11-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f11-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b6f11-115">Requirements</span></span>



| <span data-ttu-id="b6f11-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b6f11-116">Requirement</span></span> | <span data-ttu-id="b6f11-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b6f11-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b6f11-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6f11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f11-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6f11-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b6f11-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6f11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f11-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6f11-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b6f11-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6f11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6f11-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6f11-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f11-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6f11-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f11-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="b6f11-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b6f11-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="b6f11-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





