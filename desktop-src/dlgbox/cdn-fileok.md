---
title: Код уведомления CDN_FILEOK (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя, когда пользователь указывает имя файла и нажимает кнопку ОК.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672815"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="3d0f7-104">\_Код уведомления ФИЛЕОК CDN</span><span class="sxs-lookup"><span data-stu-id="3d0f7-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="3d0f7-105">Отсылается диалоговым окном **открытия** или **сохранения** в стиле обозревателя, когда пользователь указывает имя файла и нажимает кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="3d0f7-106">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="3d0f7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d0f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d0f7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d0f7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d0f7-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3d0f7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d0f7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d0f7-111">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="3d0f7-112">Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ филеок CDN** .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="3d0f7-113">Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) также содержит указатель на структуру [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , член **указанный** которой указывает адрес выбранного имени файла.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d0f7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d0f7-114">Return value</span></span>

<span data-ttu-id="3d0f7-115">Если процедура-обработчик возвращает значение 0, диалоговое окно принимает указанное имя файла и закрывается.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="3d0f7-116">Чтобы отклонить указанное имя файла и принудительно оставить диалоговое окно открытым, возвращайте ненулевое значение из процедуры-ловушки и вызовите функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , чтобы установить ненулевое значение **\_ мсгресулт DWL** .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d0f7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d0f7-117">Remarks</span></span>

<span data-ttu-id="3d0f7-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d0f7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3d0f7-119">Requirements</span></span>



| <span data-ttu-id="3d0f7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3d0f7-120">Requirement</span></span> | <span data-ttu-id="3d0f7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3d0f7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0f7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d0f7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d0f7-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d0f7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d0f7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d0f7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d0f7-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d0f7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d0f7-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d0f7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d0f7-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d0f7-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d0f7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d0f7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d0f7-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3d0f7-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="3d0f7-131">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="3d0f7-132">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="3d0f7-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="3d0f7-133">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="3d0f7-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="3d0f7-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="3d0f7-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d0f7-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="3d0f7-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="3d0f7-138">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3d0f7-139">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="3d0f7-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

