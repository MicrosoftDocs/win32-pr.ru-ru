---
description: Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска). Счетчик включает файлы с длинными именами файлов.
title: Сообщение FM_GETSELCOUNTLFN (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997746"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="cab0e-104">\_Сообщение FM жетселкаунтлфн</span><span class="sxs-lookup"><span data-stu-id="cab0e-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="cab0e-105">Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="cab0e-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="cab0e-106">Счетчик включает файлы с длинными именами файлов.</span><span class="sxs-lookup"><span data-stu-id="cab0e-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="cab0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cab0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab0e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cab0e-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cab0e-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cab0e-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cab0e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cab0e-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cab0e-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cab0e-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab0e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cab0e-112">Return value</span></span>

<span data-ttu-id="cab0e-113">Возвращает число выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="cab0e-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab0e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cab0e-114">Remarks</span></span>

<span data-ttu-id="cab0e-115">Только расширения, поддерживающие длинные имена файлов (например, сетевые расширения), должны использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="cab0e-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab0e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cab0e-116">Requirements</span></span>



| <span data-ttu-id="cab0e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cab0e-117">Requirement</span></span> | <span data-ttu-id="cab0e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cab0e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cab0e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cab0e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cab0e-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cab0e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cab0e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cab0e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cab0e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cab0e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cab0e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cab0e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab0e-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab0e-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab0e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cab0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab0e-126">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="cab0e-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="cab0e-127">**FM \_ жетфилеселлфн**</span><span class="sxs-lookup"><span data-stu-id="cab0e-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="cab0e-128">**FM \_ жетселкаунт**</span><span class="sxs-lookup"><span data-stu-id="cab0e-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




