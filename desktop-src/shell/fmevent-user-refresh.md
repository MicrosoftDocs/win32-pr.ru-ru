---
description: Отправляется в библиотеку DLL расширения, когда пользователь выбирает команду "Обновить" из меню "вид" в диспетчере файлов. Расширение может использовать это уведомление для обновления меню.
title: Сообщение FMEVENT_USER_REFRESH (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985512"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="71420-104">\_ \_ Сообщение об обновлении пользователя фмевент</span><span class="sxs-lookup"><span data-stu-id="71420-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="71420-105">Отправляется в библиотеку DLL расширения, когда пользователь выбирает команду " **Обновить** " из меню " **вид** " в диспетчере файлов.</span><span class="sxs-lookup"><span data-stu-id="71420-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="71420-106">Расширение может использовать это уведомление для обновления меню.</span><span class="sxs-lookup"><span data-stu-id="71420-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="71420-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71420-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71420-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71420-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="71420-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="71420-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="71420-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71420-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="71420-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="71420-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71420-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71420-112">Return value</span></span>

<span data-ttu-id="71420-113">Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="71420-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="71420-114">Требования</span><span class="sxs-lookup"><span data-stu-id="71420-114">Requirements</span></span>



| <span data-ttu-id="71420-115">Требование</span><span class="sxs-lookup"><span data-stu-id="71420-115">Requirement</span></span> | <span data-ttu-id="71420-116">Значение</span><span class="sxs-lookup"><span data-stu-id="71420-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71420-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71420-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71420-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71420-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="71420-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71420-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71420-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71420-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71420-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="71420-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71420-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="71420-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71420-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71420-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71420-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="71420-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




