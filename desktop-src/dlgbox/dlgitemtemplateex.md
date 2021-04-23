---
title: Структура ДЛГИТЕМТЕМПЛАТИКС
description: Блок текста, используемый расширенным шаблоном диалогового окна для описания расширенного диалогового окна. Описание формата расширенного шаблона диалогового окна см. в разделе ДЛГТЕМПЛАТИКС.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Диалоговые окна структуры ДЛГИТЕМТЕМПЛАТИКС
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416089"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="1d308-105">Структура ДЛГИТЕМТЕМПЛАТИКС</span><span class="sxs-lookup"><span data-stu-id="1d308-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="1d308-106">Блок текста, используемый расширенным шаблоном диалогового окна для описания расширенного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1d308-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="1d308-107">Описание формата расширенного шаблона диалогового окна см. в разделе [**длгтемплатикс**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="1d308-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d308-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d308-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="1d308-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1d308-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d308-110">**Идентификатор справки**</span><span class="sxs-lookup"><span data-stu-id="1d308-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d308-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-112">Идентификатор контекста справки для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-112">The help context identifier for the control.</span></span> <span data-ttu-id="1d308-113">Когда система отправляет [**\_ справочное сообщение WM**](../shell/wm-help.md) , она передает значение **идентификатор справки** в элемент **двконтекстид** структуры [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="1d308-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-114">**Операторе EXSTYLE**</span><span class="sxs-lookup"><span data-stu-id="1d308-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d308-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-116">Расширенные стили для окна.</span><span class="sxs-lookup"><span data-stu-id="1d308-116">The extended styles for a window.</span></span> <span data-ttu-id="1d308-117">Этот элемент не используется для создания элементов управления в диалоговых окнах, но приложения, использующие шаблоны диалоговых окон, могут использовать его для создания других типов окон.</span><span class="sxs-lookup"><span data-stu-id="1d308-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="1d308-118">Список значений см. в разделе [**Расширенные стили окон**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="1d308-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="1d308-119">**style**</span><span class="sxs-lookup"><span data-stu-id="1d308-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-120">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d308-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-121">Стиль элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-121">The style of the control.</span></span> <span data-ttu-id="1d308-122">Этот элемент может представлять собой сочетание [значений стиля окна](/windows/desktop/winmsg/window-styles) (например, **WS \_ border**) и одного или нескольких [значений стиля элемента управления](/windows/desktop/Controls/common-control-styles) (таких как **\_ кнопки BS** и **\_ Left**).</span><span class="sxs-lookup"><span data-stu-id="1d308-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="1d308-123">**x**</span><span class="sxs-lookup"><span data-stu-id="1d308-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-124">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="1d308-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-125">Координата x (в диалоговых окнах) верхнего левого угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="1d308-126">Эта координата всегда указывается относительно левого верхнего угла клиентской области диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1d308-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-127">**y**</span><span class="sxs-lookup"><span data-stu-id="1d308-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-128">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="1d308-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-129">Координата y (в диалоговых окнах) верхнего левого угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="1d308-130">Эта координата всегда указывается относительно левого верхнего угла клиентской области диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1d308-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-131">**/CX**</span><span class="sxs-lookup"><span data-stu-id="1d308-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-132">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="1d308-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-133">Ширина (в диалоговых окнах) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-134">**CY**</span><span class="sxs-lookup"><span data-stu-id="1d308-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-135">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="1d308-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-136">Высота (в диалоговых окнах) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-137">**id**</span><span class="sxs-lookup"><span data-stu-id="1d308-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-138">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d308-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-139">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-140">**виндовкласс**</span><span class="sxs-lookup"><span data-stu-id="1d308-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-141">Тип: **SZ \_ или \_**</span><span class="sxs-lookup"><span data-stu-id="1d308-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-142">Массив из 16-разрядных элементов переменной длины, указывающий класс окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="1d308-143">Если первый элемент массива имеет любое значение, отличное от 0xFFFF, система рассматривает массив как строку в Юникоде, заканчивающуюся нулем, которая указывает имя зарегистрированного класса окна.</span><span class="sxs-lookup"><span data-stu-id="1d308-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="1d308-144">Если первый элемент имеет значение 0xFFFF, в массиве имеется один дополнительный элемент, указывающий порядковый номер предопределенного системного класса.</span><span class="sxs-lookup"><span data-stu-id="1d308-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="1d308-145">Порядковый номер может быть одним из следующих значений Atom.</span><span class="sxs-lookup"><span data-stu-id="1d308-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="1d308-146">Значение</span><span class="sxs-lookup"><span data-stu-id="1d308-146">Value</span></span>                                                                             | <span data-ttu-id="1d308-147">Значение</span><span class="sxs-lookup"><span data-stu-id="1d308-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="1d308-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="1d308-149">Кнопка</span><span class="sxs-lookup"><span data-stu-id="1d308-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="1d308-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="1d308-151">Изменить</span><span class="sxs-lookup"><span data-stu-id="1d308-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="1d308-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="1d308-153">Статические</span><span class="sxs-lookup"><span data-stu-id="1d308-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="1d308-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="1d308-155">Список</span><span class="sxs-lookup"><span data-stu-id="1d308-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="1d308-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="1d308-157">полоса прокрутки;</span><span class="sxs-lookup"><span data-stu-id="1d308-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="1d308-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="1d308-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="1d308-159">поле со списком;</span><span class="sxs-lookup"><span data-stu-id="1d308-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="1d308-160">**title**</span><span class="sxs-lookup"><span data-stu-id="1d308-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-161">Тип: **SZ \_ или \_**</span><span class="sxs-lookup"><span data-stu-id="1d308-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-162">Массив с переменной длиной из 16-разрядных элементов, который содержит исходный текст или идентификатор ресурса элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="1d308-163">Если первый элемент массива имеет значение 0xFFFF, то массив содержит один дополнительный элемент, указывающий порядковый номер ресурса, например значка, в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="1d308-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="1d308-164">Можно использовать идентификатор ресурса для элементов управления, таких как статические элементы управления "значок", которые загружают и отображают значок или другой ресурс, а не текст.</span><span class="sxs-lookup"><span data-stu-id="1d308-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="1d308-165">Если первый элемент имеет любое значение, отличное от 0xFFFF, система рассматривает массив как строку в Юникоде, заканчивающуюся нулем, которая указывает начальный текст.</span><span class="sxs-lookup"><span data-stu-id="1d308-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="1d308-166">**екстракаунт**</span><span class="sxs-lookup"><span data-stu-id="1d308-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="1d308-167">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1d308-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1d308-168">Число байтов данных создания, которые следуют за данным элементом.</span><span class="sxs-lookup"><span data-stu-id="1d308-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="1d308-169">Если это значение больше нуля, то данные для создания начинаются со следующей границы **слова** .</span><span class="sxs-lookup"><span data-stu-id="1d308-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="1d308-170">Данные создания могут иметь любой размер и формат.</span><span class="sxs-lookup"><span data-stu-id="1d308-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="1d308-171">Процедура окна элемента управления должна иметь возможность интерпретировать данные.</span><span class="sxs-lookup"><span data-stu-id="1d308-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="1d308-172">Когда система создает элемент управления, она передает указатель на эти данные в параметре *lParam* сообщения [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) , которое отправляется в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1d308-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d308-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d308-173">Remarks</span></span>

<span data-ttu-id="1d308-174">Расширенный шаблон для диалогового окна состоит из заголовка [**длгтемплатикс**](dlgtemplateex.md) , за которым следует структура **длгитемтемплатикс** для каждого элемента управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="1d308-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="1d308-175">Каждая структура **длгитемтемплатикс** должна быть согласована на границе **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1d308-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="1d308-176">Массивы **виндовкласс** и **Title** переменной длины должны быть согласованы по границам **слов** .</span><span class="sxs-lookup"><span data-stu-id="1d308-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="1d308-177">Массив данных создания, если он имеется, должен быть согласован по границе **слова** .</span><span class="sxs-lookup"><span data-stu-id="1d308-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="1d308-178">Если в массивах **виндовкласс** и **Title** указываются символьные строки, необходимо использовать строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1d308-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="1d308-179">Используйте функцию [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) для создания строк Юникода из строк ANSI.</span><span class="sxs-lookup"><span data-stu-id="1d308-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="1d308-180">Члены **x**, **y**, **CX** и **CY** задают значения в диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="1d308-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="1d308-181">Эти значения можно преобразовать в единицы экрана (в пикселях) с помощью функции [**мапдиалогрект**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="1d308-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d308-182">Требования</span><span class="sxs-lookup"><span data-stu-id="1d308-182">Requirements</span></span>



| <span data-ttu-id="1d308-183">Требование</span><span class="sxs-lookup"><span data-stu-id="1d308-183">Requirement</span></span> | <span data-ttu-id="1d308-184">Значение</span><span class="sxs-lookup"><span data-stu-id="1d308-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1d308-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d308-185">Minimum supported client</span></span><br/> | <span data-ttu-id="1d308-186">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d308-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1d308-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d308-187">Minimum supported server</span></span><br/> | <span data-ttu-id="1d308-188">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d308-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1d308-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d308-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d308-190">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1d308-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d308-191">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="1d308-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="1d308-192">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="1d308-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="1d308-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="1d308-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="1d308-194">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="1d308-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="1d308-195">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="1d308-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="1d308-196">**длгтемплатикс**</span><span class="sxs-lookup"><span data-stu-id="1d308-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="1d308-197">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="1d308-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="1d308-198">**\_Создание WM**</span><span class="sxs-lookup"><span data-stu-id="1d308-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="1d308-199">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1d308-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d308-200">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="1d308-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="1d308-201">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="1d308-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1d308-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="1d308-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="1d308-203">**\_Справка WM**</span><span class="sxs-lookup"><span data-stu-id="1d308-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

