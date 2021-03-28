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
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262785"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="30952-103">\_ \_ Сообщение об обновлении Windows FM</span><span class="sxs-lookup"><span data-stu-id="30952-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="30952-104">Посылается расширением диспетчера файлов для того, чтобы диспетчер файлов перезаводился как активное окно или все его окна.</span><span class="sxs-lookup"><span data-stu-id="30952-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="30952-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="30952-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30952-106">*фрепаинт*</span><span class="sxs-lookup"><span data-stu-id="30952-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="30952-107">Значение, указывающее, перерисовывается ли диспетчером файлов активное окно или все его окна.</span><span class="sxs-lookup"><span data-stu-id="30952-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="30952-108">Если этот параметр имеет **значение true**, диспетчер файлов перерисовывает все окна.</span><span class="sxs-lookup"><span data-stu-id="30952-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="30952-109">В противном случае диспетчер файлов перерисовывает только активное окно.</span><span class="sxs-lookup"><span data-stu-id="30952-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="30952-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30952-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="30952-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="30952-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30952-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30952-112">Return value</span></span>

<span data-ttu-id="30952-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="30952-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30952-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="30952-114">Remarks</span></span>

<span data-ttu-id="30952-115">Изменения файловой системы, вызванные расширением, автоматически обнаруживаются диспетчером файлов.</span><span class="sxs-lookup"><span data-stu-id="30952-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="30952-116">Расширение должно использовать это сообщение только в тех случаях, когда выполняется или отменяется подключение к диску.</span><span class="sxs-lookup"><span data-stu-id="30952-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="30952-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30952-117">Requirements</span></span>



| <span data-ttu-id="30952-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30952-118">Requirement</span></span> | <span data-ttu-id="30952-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30952-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30952-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30952-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30952-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30952-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="30952-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30952-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30952-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30952-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30952-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30952-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30952-125"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="30952-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30952-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30952-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30952-127">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="30952-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




