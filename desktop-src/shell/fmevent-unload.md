---
description: Отправляется в библиотеку DLL расширения, когда диспетчер файлов выгружает библиотеку DLL.
title: Сообщение FMEVENT_UNLOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143072"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="4cfb2-103">\_Сообщение о выгрузке фмевент</span><span class="sxs-lookup"><span data-stu-id="4cfb2-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="4cfb2-104">Отправляется в библиотеку DLL расширения, когда диспетчер файлов выгружает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cfb2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cfb2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfb2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cfb2-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4cfb2-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4cfb2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cfb2-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4cfb2-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfb2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cfb2-110">Return value</span></span>

<span data-ttu-id="4cfb2-111">Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfb2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cfb2-112">Remarks</span></span>

<span data-ttu-id="4cfb2-113">Значения *HWND* и **HMENU** , передаваемые с помощью [**фмевент \_ Load**](fmevent-load.md) и [**фмевент \_ инитмену**](fmevent-initmenu.md) messages, могут быть недействительны во время отправки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfb2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4cfb2-114">Requirements</span></span>



| <span data-ttu-id="4cfb2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4cfb2-115">Requirement</span></span> | <span data-ttu-id="4cfb2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4cfb2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfb2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cfb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4cfb2-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cfb2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4cfb2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cfb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4cfb2-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cfb2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4cfb2-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4cfb2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cfb2-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb2-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cfb2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cfb2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfb2-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="4cfb2-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




