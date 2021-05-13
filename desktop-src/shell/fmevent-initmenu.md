---
description: Отправляется в библиотеку DLL расширения, когда пользователь выбирает меню для расширения из строки меню диспетчера файлов. Расширение может использовать это уведомление для инициализации пунктов меню.
title: Сообщение FMEVENT_INITMENU (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842285"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="84633-104">\_Сообщение фмевент инитмену</span><span class="sxs-lookup"><span data-stu-id="84633-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="84633-105">Отправляется в библиотеку DLL расширения, когда пользователь выбирает меню для расширения из строки меню диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="84633-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="84633-106">Расширение может использовать это уведомление для инициализации пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="84633-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="84633-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="84633-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84633-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84633-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84633-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="84633-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84633-110">*HMENU*</span><span class="sxs-lookup"><span data-stu-id="84633-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="84633-111">Маркер строки меню диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="84633-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84633-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84633-112">Return value</span></span>

<span data-ttu-id="84633-113">Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="84633-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="84633-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="84633-114">Remarks</span></span>

<span data-ttu-id="84633-115">Библиотека DLL расширения получает это сообщение, только когда пользователь выбирает меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="84633-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="84633-116">Если расширение содержит подменю, оно должно инициализировать их одновременно с инициализацией меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="84633-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="84633-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="84633-117">Requirements</span></span>



| <span data-ttu-id="84633-118">Требование</span><span class="sxs-lookup"><span data-stu-id="84633-118">Requirement</span></span> | <span data-ttu-id="84633-119">Значение</span><span class="sxs-lookup"><span data-stu-id="84633-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84633-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84633-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84633-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84633-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="84633-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84633-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84633-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84633-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84633-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="84633-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84633-125"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="84633-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84633-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84633-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84633-127">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="84633-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




