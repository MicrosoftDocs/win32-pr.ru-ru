---
title: Сообщение ЛБСЕЛЧСТРИНГ (Коммдлг. h)
description: Диалоговое окно Открыть или сохранить как отправляет зарегистрированное сообщение ЛБСЕЛЧСТРИНГ в процедуру-обработчик при изменении выбора в любом из списков или полей со списком диалогового окна.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Диалоговые окна сообщения ЛБСЕЛЧСТРИНГ
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590771"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="4f25b-104">Сообщение ЛБСЕЛЧСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="4f25b-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="4f25b-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="4f25b-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="4f25b-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="4f25b-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4f25b-107">Диалоговое окно **Открыть** или **Сохранить как** отправляет зарегистрированное сообщение **лбселчстринг** в процедуру-обработчик при изменении выбора в любом из списков или полей со списком диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4f25b-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="4f25b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f25b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f25b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f25b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f25b-110">Идентификатор списка или поля со списком, в котором был изменен выбор.</span><span class="sxs-lookup"><span data-stu-id="4f25b-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="4f25b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f25b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f25b-112">Слово нижнего порядка задает номер позиции выбранной строки в списке или поле со списком.</span><span class="sxs-lookup"><span data-stu-id="4f25b-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="4f25b-113">Слово в высоком порядке указывает тип изменения выбора.</span><span class="sxs-lookup"><span data-stu-id="4f25b-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="4f25b-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="4f25b-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4f25b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4f25b-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="4f25b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4f25b-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="4f25b-117"><dt>**Компакт-диск \_ ЛБСЕЛЧАНЖЕ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f25b-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="4f25b-118">Элемент является единственным элементом, выбранным в списке с единственным выбором.</span><span class="sxs-lookup"><span data-stu-id="4f25b-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="4f25b-119"><dt>**Компакт-диск \_ ЛБСЕЛАДД**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f25b-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="4f25b-120">Элемент является одним из элементов, выбранных в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="4f25b-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="4f25b-121"><dt>**Компакт-диск \_ ЛБСЕЛСУБ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f25b-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="4f25b-122">Элемент больше не выбирается в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="4f25b-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="4f25b-123"><dt>**Компакт-диск \_ ЛБСЕЛНОИТЕМС**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="4f25b-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="4f25b-124">В списке с множественным выбором не существует элементов.</span><span class="sxs-lookup"><span data-stu-id="4f25b-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f25b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f25b-125">Return value</span></span>

<span data-ttu-id="4f25b-126">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4f25b-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f25b-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f25b-127">Remarks</span></span>

<span data-ttu-id="4f25b-128">Процедура-обработчик должна указать константу **лбселчстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , чтобы получить идентификатор сообщения, отправленного диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="4f25b-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f25b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4f25b-129">Requirements</span></span>



| <span data-ttu-id="4f25b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4f25b-130">Requirement</span></span> | <span data-ttu-id="4f25b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4f25b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f25b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f25b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4f25b-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f25b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4f25b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f25b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4f25b-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f25b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f25b-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f25b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f25b-137"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f25b-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4f25b-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4f25b-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f25b-139">**Лбселчстрингв** (Юникод) и **лбселчстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f25b-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="4f25b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f25b-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f25b-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4f25b-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4f25b-142">**\_СЕЛЧАНЖЕ CDN**</span><span class="sxs-lookup"><span data-stu-id="4f25b-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="4f25b-143">**\_ТИПЕЧАНЖЕ CDN**</span><span class="sxs-lookup"><span data-stu-id="4f25b-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="4f25b-144">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="4f25b-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="4f25b-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4f25b-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4f25b-146">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="4f25b-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

