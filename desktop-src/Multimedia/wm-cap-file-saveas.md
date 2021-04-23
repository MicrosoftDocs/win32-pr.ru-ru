---
title: Сообщение WM_CAP_FILE_SAVEAS (VFW. h)
description: '\_Сообщение SAVEAS с закреплением WM \_ \_ копирует содержимое файла записи в другой файл. Это сообщение можно отправить явно или с помощью макроса Капфилесавеас.'
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415133"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="d7656-105">\_Сообщение о \_ SAVEAS для файла ЗАкрепления WM \_</span><span class="sxs-lookup"><span data-stu-id="d7656-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="d7656-106">Сообщение **\_ \_ \_ SAVEAS с закреплением WM** копирует содержимое файла записи в другой файл.</span><span class="sxs-lookup"><span data-stu-id="d7656-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="d7656-107">Это сообщение можно отправить явно или с помощью макроса [**капфилесавеас**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .</span><span class="sxs-lookup"><span data-stu-id="d7656-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="d7656-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7656-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7656-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="d7656-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="d7656-110">Указатель на строку, завершающуюся нулем, которая содержит имя целевого файла, используемого для копирования файла.</span><span class="sxs-lookup"><span data-stu-id="d7656-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7656-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7656-111">Return Value</span></span>

<span data-ttu-id="d7656-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d7656-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="d7656-113">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="d7656-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7656-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7656-114">Remarks</span></span>

<span data-ttu-id="d7656-115">Это сообщение не изменяет имя или содержимое текущего файла записи.</span><span class="sxs-lookup"><span data-stu-id="d7656-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="d7656-116">Если операция копирования завершается неудачно из-за ошибки переполнения диска, конечный файл автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="d7656-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="d7656-117">Как правило, файл записи предварительно выделяется для самого крупного сегмента записи, и только его часть может использоваться для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="d7656-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="d7656-118">В этом сообщении копируется только часть файла, содержащего данные записи.</span><span class="sxs-lookup"><span data-stu-id="d7656-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7656-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d7656-119">Requirements</span></span>



| <span data-ttu-id="d7656-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d7656-120">Requirement</span></span> | <span data-ttu-id="d7656-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d7656-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7656-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7656-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7656-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7656-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7656-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7656-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7656-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7656-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7656-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7656-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7656-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7656-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7656-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7656-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7656-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="d7656-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d7656-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d7656-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





