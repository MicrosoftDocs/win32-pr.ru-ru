---
title: Сообщение DM_GETDEFID (Winuser. h)
description: Извлекает идентификатор элемента управления "Кнопка" по умолчанию для диалогового окна.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID диалоговых окон сообщений
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535267"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="62cde-104">\_Сообщение ЖЕТДЕФИД DM</span><span class="sxs-lookup"><span data-stu-id="62cde-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="62cde-105">Извлекает идентификатор элемента управления "Кнопка" по умолчанию для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="62cde-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="62cde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62cde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62cde-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62cde-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62cde-108">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="62cde-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="62cde-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62cde-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62cde-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="62cde-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62cde-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62cde-111">Return value</span></span>

<span data-ttu-id="62cde-112">Если существует кнопка отправки по умолчанию, то в верхнем порядке слово возвращаемого значения будет содержаться значение **DC \_ хасдефид** , а в слове с низким порядком — идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="62cde-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="62cde-113">В противном случае возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="62cde-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="62cde-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62cde-114">Remarks</span></span>

<span data-ttu-id="62cde-115">Функция [**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="62cde-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cde-116">Требования</span><span class="sxs-lookup"><span data-stu-id="62cde-116">Requirements</span></span>



| <span data-ttu-id="62cde-117">Требование</span><span class="sxs-lookup"><span data-stu-id="62cde-117">Requirement</span></span> | <span data-ttu-id="62cde-118">Значение</span><span class="sxs-lookup"><span data-stu-id="62cde-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cde-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62cde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62cde-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62cde-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62cde-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62cde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62cde-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62cde-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62cde-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="62cde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62cde-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62cde-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cde-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62cde-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="62cde-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="62cde-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62cde-127">**дефдлгпрок**</span><span class="sxs-lookup"><span data-stu-id="62cde-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="62cde-128">**\_СЕТДЕФИД DM**</span><span class="sxs-lookup"><span data-stu-id="62cde-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="62cde-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="62cde-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62cde-130">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="62cde-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





