---
title: Сообщение КОЛОРОКСТРИНГ (Коммдлг. h)
description: Диалоговое окно цвета отправляет зарегистрированное сообщение КОЛОРОКСТРИНГ в процедуру-обработчик, Кчукпрок, когда пользователь выбирает цвет и нажимает кнопку ОК.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Диалоговые окна сообщения КОЛОРОКСТРИНГ
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135878"
---
# <a name="colorokstring-message"></a><span data-ttu-id="315dc-104">Сообщение КОЛОРОКСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="315dc-104">COLOROKSTRING message</span></span>

<span data-ttu-id="315dc-105">Диалоговое окно **цвета** отправляет зарегистрированное сообщение **колорокстринг** в процедуру-обработчик, [*кчукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), когда пользователь выбирает цвет и нажимает кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="315dc-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="315dc-106">Процедура-обработчик может принять цвет и разрешить закрытие диалогового окна или отклонить цвет и принудительно оставить диалоговое окно открытым.</span><span class="sxs-lookup"><span data-stu-id="315dc-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="315dc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="315dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315dc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="315dc-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="315dc-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="315dc-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="315dc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="315dc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="315dc-111">Указатель на структуру [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .</span><span class="sxs-lookup"><span data-stu-id="315dc-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="315dc-112">Элемент **ргбресулт** этой структуры содержит значение цвета RGB выбранного цвета.</span><span class="sxs-lookup"><span data-stu-id="315dc-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315dc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="315dc-113">Return value</span></span>

<span data-ttu-id="315dc-114">Если процедура-обработчик возвращает значение 0, то диалоговое окно **Цвет** принимает выбранный цвет и закрывается.</span><span class="sxs-lookup"><span data-stu-id="315dc-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="315dc-115">Если процедура-обработчик возвращает ненулевое значение, то диалоговое окно **Цвет** отклоняет выбранный цвет и остается открытым.</span><span class="sxs-lookup"><span data-stu-id="315dc-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="315dc-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="315dc-116">Remarks</span></span>

<span data-ttu-id="315dc-117">Процедура-ловушка должна указывать константу **колорокстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) для получения идентификатора сообщения, отправленного этим диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="315dc-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="315dc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="315dc-118">Requirements</span></span>



| <span data-ttu-id="315dc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="315dc-119">Requirement</span></span> | <span data-ttu-id="315dc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="315dc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="315dc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="315dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="315dc-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="315dc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="315dc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="315dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="315dc-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="315dc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="315dc-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="315dc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="315dc-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="315dc-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="315dc-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="315dc-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="315dc-128">**Колорокстрингв** (Юникод) и **колорокстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="315dc-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="315dc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="315dc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="315dc-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="315dc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="315dc-131">**чусеколор**</span><span class="sxs-lookup"><span data-stu-id="315dc-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="315dc-132">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="315dc-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="315dc-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="315dc-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="315dc-134">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="315dc-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

