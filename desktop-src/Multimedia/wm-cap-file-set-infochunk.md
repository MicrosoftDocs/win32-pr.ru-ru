---
title: Сообщение WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: '\_ \_ \_ Сообщение инфочунк Set WM Cap \_ устанавливает и очищает информационные блоки.'
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071150"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="1b1bc-104">\_Сообщение о \_ \_ задании файла \_ ИНФОЧУНК с ограничением WM</span><span class="sxs-lookup"><span data-stu-id="1b1bc-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="1b1bc-105">Сообщение **\_ \_ \_ \_ инфочунк Set WM Cap** устанавливает и очищает информационные блоки.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="1b1bc-106">Фрагменты информации могут быть вставлены в файл AVI во время записи, чтобы внедрять текстовые строки или пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="1b1bc-107">Это сообщение можно отправить явно или с помощью макроса [**капфилесетинфочунк**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="1b1bc-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="1b1bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b1bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1bc-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*лпинфочунк*</span><span class="sxs-lookup"><span data-stu-id="1b1bc-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="1b1bc-110">Указатель на структуру [**капинфочунк**](/windows/win32/api/vfw/ns-vfw-capinfochunk) , определяющую создаваемый или удаляемый блок сведений.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1bc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b1bc-111">Return Value</span></span>

<span data-ttu-id="1b1bc-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="1b1bc-113">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b1bc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b1bc-114">Remarks</span></span>

<span data-ttu-id="1b1bc-115">В файл AVI можно добавить несколько блоков зарегистрированных данных.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="1b1bc-116">После установки информационного блока он добавляется в последующие файлы записи до тех пор, пока не будет снята запись или не будут удалены все записи фрагментов данных.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="1b1bc-117">Чтобы очистить одну запись, укажите фрагмент данных в элементе **фкЦинфоид** и **значение NULL** в элементе **лпдата** структуры [**капинфочунк**](/windows/win32/api/vfw/ns-vfw-capinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="1b1bc-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="1b1bc-118">Чтобы очистить все записи, укажите **значение NULL** в **фкЦинфоид**.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1b1bc-119">Requirements</span></span>



| <span data-ttu-id="1b1bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1b1bc-120">Requirement</span></span> | <span data-ttu-id="1b1bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1b1bc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1b1bc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b1bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1bc-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b1bc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1b1bc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b1bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1bc-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b1bc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1b1bc-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1b1bc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1bc-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b1bc-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1bc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b1bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1bc-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="1b1bc-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1b1bc-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="1b1bc-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





