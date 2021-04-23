---
title: Сообщение ФИЛЕОКСТРИНГ (Коммдлг. h)
description: Диалоговое окно Открыть или сохранить как отправляет зарегистрированное сообщение ФИЛЕОКСТРИНГ в процедуру-обработчик, Офнхукпрок, когда пользователь указывает имя файла и нажимает кнопку ОК.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Диалоговые окна сообщения ФИЛЕОКСТРИНГ
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6fddbb3460f15e1efb946b9bd17f1c85fd031a8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590791"
---
# <a name="fileokstring-message"></a><span data-ttu-id="832e8-104">Сообщение ФИЛЕОКСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="832e8-104">FILEOKSTRING message</span></span>

<span data-ttu-id="832e8-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="832e8-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="832e8-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="832e8-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="832e8-107">Диалоговое окно **Открыть** или **Сохранить как** отправляет зарегистрированное сообщение **филеокстринг** в процедуру-обработчик, [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), когда пользователь указывает имя файла и нажимает кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="832e8-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="832e8-108">Процедура-обработчик может принять имя файла и разрешить диалоговое окно закрыть или отклонить имя файла и принудительно оставить диалоговое окно открытым.</span><span class="sxs-lookup"><span data-stu-id="832e8-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="832e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="832e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832e8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="832e8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="832e8-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="832e8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="832e8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="832e8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="832e8-113">Указатель на структуру [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="832e8-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="832e8-114">Член **указанный** этой структуры содержит диск, путь и имя файла, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="832e8-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="832e8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="832e8-115">Return value</span></span>

<span data-ttu-id="832e8-116">Если процедура-обработчик возвращает значение 0, диалоговое окно **Открыть** или **Сохранить как** принимает указанное имя файла и закрывается.</span><span class="sxs-lookup"><span data-stu-id="832e8-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="832e8-117">Если процедура-обработчик возвращает ненулевое значение, то диалоговое окно **Открыть** или **Сохранить как** отклоняет указанное имя файла и остается открытым.</span><span class="sxs-lookup"><span data-stu-id="832e8-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="832e8-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="832e8-118">Remarks</span></span>

<span data-ttu-id="832e8-119">Процедура-обработчик должна указать константу **филеокстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , чтобы получить идентификатор сообщения, отправленного диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="832e8-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="832e8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="832e8-120">Requirements</span></span>



| <span data-ttu-id="832e8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="832e8-121">Requirement</span></span> | <span data-ttu-id="832e8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="832e8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="832e8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="832e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="832e8-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="832e8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="832e8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="832e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="832e8-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="832e8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="832e8-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="832e8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="832e8-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="832e8-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="832e8-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="832e8-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="832e8-130">**Филеокстрингв** (Юникод) и **филеокстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="832e8-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="832e8-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="832e8-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="832e8-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="832e8-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="832e8-133">**\_ФИЛЕОК CDN**</span><span class="sxs-lookup"><span data-stu-id="832e8-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="832e8-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="832e8-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="832e8-135">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="832e8-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="832e8-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="832e8-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="832e8-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="832e8-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

