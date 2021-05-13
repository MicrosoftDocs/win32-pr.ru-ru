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
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841345"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="c1a04-104">\_Сообщение FM жетселкаунтлфн</span><span class="sxs-lookup"><span data-stu-id="c1a04-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="c1a04-105">Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="c1a04-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="c1a04-106">Счетчик включает файлы с длинными именами файлов.</span><span class="sxs-lookup"><span data-stu-id="c1a04-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1a04-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1a04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a04-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1a04-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c1a04-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c1a04-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c1a04-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1a04-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c1a04-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c1a04-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a04-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1a04-112">Return value</span></span>

<span data-ttu-id="c1a04-113">Возвращает число выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="c1a04-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a04-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1a04-114">Remarks</span></span>

<span data-ttu-id="c1a04-115">Только расширения, поддерживающие длинные имена файлов (например, сетевые расширения), должны использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="c1a04-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a04-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="c1a04-116">Requirements</span></span>



| <span data-ttu-id="c1a04-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c1a04-117">Requirement</span></span> | <span data-ttu-id="c1a04-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c1a04-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a04-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1a04-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a04-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1a04-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c1a04-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1a04-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a04-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1a04-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1a04-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1a04-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1a04-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a04-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a04-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1a04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a04-126">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="c1a04-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="c1a04-127">**FM \_ жетфилеселлфн**</span><span class="sxs-lookup"><span data-stu-id="c1a04-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="c1a04-128">**FM \_ жетселкаунт**</span><span class="sxs-lookup"><span data-stu-id="c1a04-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




