---
description: Посылается расширением диспетчера файлов для того, чтобы диспетчер файлов перезаводился как активное окно или все его окна.
title: Сообщение FM_REFRESH_WINDOWS (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842355"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="0bac9-103">\_ \_ Сообщение об обновлении Windows FM</span><span class="sxs-lookup"><span data-stu-id="0bac9-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="0bac9-104">Посылается расширением диспетчера файлов для того, чтобы диспетчер файлов перезаводился как активное окно или все его окна.</span><span class="sxs-lookup"><span data-stu-id="0bac9-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="0bac9-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bac9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bac9-106">*фрепаинт*</span><span class="sxs-lookup"><span data-stu-id="0bac9-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac9-107">Значение, указывающее, перерисовывается ли диспетчером файлов активное окно или все его окна.</span><span class="sxs-lookup"><span data-stu-id="0bac9-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="0bac9-108">Если этот параметр имеет **значение true**, диспетчер файлов перерисовывает все окна.</span><span class="sxs-lookup"><span data-stu-id="0bac9-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="0bac9-109">В противном случае диспетчер файлов перерисовывает только активное окно.</span><span class="sxs-lookup"><span data-stu-id="0bac9-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="0bac9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bac9-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0bac9-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0bac9-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bac9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bac9-112">Return value</span></span>

<span data-ttu-id="0bac9-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0bac9-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bac9-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="0bac9-114">Remarks</span></span>

<span data-ttu-id="0bac9-115">Изменения файловой системы, вызванные расширением, автоматически обнаруживаются диспетчером файлов.</span><span class="sxs-lookup"><span data-stu-id="0bac9-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="0bac9-116">Расширение должно использовать это сообщение только в тех случаях, когда выполняется или отменяется подключение к диску.</span><span class="sxs-lookup"><span data-stu-id="0bac9-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bac9-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="0bac9-117">Requirements</span></span>



| <span data-ttu-id="0bac9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0bac9-118">Requirement</span></span> | <span data-ttu-id="0bac9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0bac9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bac9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bac9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0bac9-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0bac9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0bac9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bac9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0bac9-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0bac9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0bac9-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0bac9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bac9-125"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bac9-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bac9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bac9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bac9-127">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="0bac9-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




