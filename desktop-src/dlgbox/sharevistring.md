---
title: Сообщение ШАРЕВИСТРИНГ (Коммдлг. h)
description: Диалоговое окно Открыть или сохранить как отправляет зарегистрированное сообщение ШАРЕВИСТРИНГ в процедуру-обработчик, Офнхукпрок, если при нажатии пользователем кнопки ОК возникает нарушение совместного доступа для выбранного файла.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Диалоговые окна сообщения ШАРЕВИСТРИНГ
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79535b66cff62ad0f9d3fd298fdd76bfc9123a3d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590671"
---
# <a name="sharevistring-message"></a><span data-ttu-id="7f005-104">Сообщение ШАРЕВИСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="7f005-104">SHAREVISTRING message</span></span>

<span data-ttu-id="7f005-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="7f005-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="7f005-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="7f005-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="7f005-107">Диалоговое окно **Открыть** или **Сохранить как** отправляет зарегистрированное сообщение **шаревистринг** в процедуру-обработчик, [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), если при нажатии пользователем кнопки **ОК** возникает нарушение совместного доступа для выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="7f005-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="7f005-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f005-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f005-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f005-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f005-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7f005-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f005-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f005-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f005-112">Указатель на структуру [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="7f005-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="7f005-113">Элемент **указанный** этой структуры содержит имя файла, вызвавшего нарушение совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="7f005-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f005-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f005-114">Return value</span></span>

<span data-ttu-id="7f005-115">Процедура-обработчик должна возвращать одно из следующих значений, чтобы указать, как диалоговое окно должно управлять нарушением общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7f005-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="7f005-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7f005-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="7f005-117">Описание:</span><span class="sxs-lookup"><span data-stu-id="7f005-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f005-118"><dt>**ОФН \_ ШАРЕФАЛЛСРАУГХ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7f005-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7f005-119">Принять имя файла</span><span class="sxs-lookup"><span data-stu-id="7f005-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="7f005-120"><dt>**ОФН \_ ШАРЕНОВАРН**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7f005-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="7f005-121">Отклоните имя файла, но не предупреждать пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f005-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="7f005-122">Приложение отвечает за отображение предупреждающего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f005-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="7f005-123"><dt>**ОФН \_ ШАРЕВАРН**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f005-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="7f005-124">Отклоните имя файла и выводит предупреждение (тот же результат, что и при отсутствии процедур обработчика).</span><span class="sxs-lookup"><span data-stu-id="7f005-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="7f005-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="7f005-125">Remarks</span></span>

<span data-ttu-id="7f005-126">Процедура-обработчик должна указать константу **шаревистринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , чтобы получить идентификатор сообщения, отправленного диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="7f005-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="7f005-127">Диалоговое окно отправляет зарегистрированное сообщение **шаревистринг** только в том случае, если вы не указали флаг **ОФН \_ шареаваре** в элементе **flags** структуры [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7f005-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="7f005-128">Если процедура-обработчик возвращает неопределенное значение, диалоговое окно реагирует так, как если бы **ОФН \_ шареварн** был возвращен.</span><span class="sxs-lookup"><span data-stu-id="7f005-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f005-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7f005-129">Requirements</span></span>



| <span data-ttu-id="7f005-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7f005-130">Requirement</span></span> | <span data-ttu-id="7f005-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7f005-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f005-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f005-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7f005-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f005-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7f005-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f005-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7f005-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f005-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f005-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f005-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f005-137"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f005-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7f005-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7f005-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f005-139">**Шаревистрингв** (Юникод) и **шаревистринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7f005-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="7f005-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f005-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f005-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7f005-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f005-142">**\_ШАРЕВИОЛАТИОН CDN**</span><span class="sxs-lookup"><span data-stu-id="7f005-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="7f005-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="7f005-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="7f005-144">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="7f005-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="7f005-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7f005-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f005-146">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="7f005-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

