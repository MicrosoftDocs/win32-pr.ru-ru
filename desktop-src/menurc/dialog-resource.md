---
title: Ресурс ДИАЛОГового окна
description: Определяет диалоговое окно. | Ресурс ДИАЛОГового окна
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Меню ресурсов ДИАЛОГовых окон и другие ресурсы
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674595"
---
# <a name="dialog-resource"></a><span data-ttu-id="eab04-105">Ресурс ДИАЛОГового окна</span><span class="sxs-lookup"><span data-stu-id="eab04-105">DIALOG resource</span></span>

<span data-ttu-id="eab04-106">Определяет диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="eab04-106">Defines a dialog box.</span></span> <span data-ttu-id="eab04-107">Оператор определяет расположение и размеры диалогового окна на экране, а также стиль диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="eab04-108">**Диалоговое окно** является УСТАРЕВШИм идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="eab04-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="eab04-109">Новые приложения должны использовать [**диаложекс**](dialogex-resource.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="eab04-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab04-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="eab04-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="eab04-112">Уникальное имя или уникальное 16-битовое целочисленное значение без знака, идентифицирующее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="eab04-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="eab04-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="eab04-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="eab04-114">Параметры для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-114">Options for the dialog box.</span></span> <span data-ttu-id="eab04-115">Это может быть ноль или более следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="eab04-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="eab04-116">Инструкция</span><span class="sxs-lookup"><span data-stu-id="eab04-116">Statement</span></span>                                                        | <span data-ttu-id="eab04-117">Описание</span><span class="sxs-lookup"><span data-stu-id="eab04-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab04-118">[**Заголовок**](caption-statement.md) "*Text*"</span><span class="sxs-lookup"><span data-stu-id="eab04-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="eab04-119">Заголовок диалогового окна, если у него есть заголовок.</span><span class="sxs-lookup"><span data-stu-id="eab04-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="eab04-120">Дополнительные сведения см. в разделе [**Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="eab04-121">[**Параметры**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="eab04-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="eab04-122">Определяемое пользователем значение **DWORD** для использования инструментами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eab04-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="eab04-123">Это значение не используется системой.</span><span class="sxs-lookup"><span data-stu-id="eab04-123">This value is not used by the system.</span></span> <span data-ttu-id="eab04-124">Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="eab04-125">[](class-statement.md) *Класс* класса</span><span class="sxs-lookup"><span data-stu-id="eab04-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="eab04-126">16-разрядное целое число без знака или строка, заключенная в двойные кавычки ("), которая определяет класс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="eab04-127">Дополнительные сведения см. в разделе [**класс**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="eab04-128">**Операторе EXSTYLE =** *Расширенные стили*</span><span class="sxs-lookup"><span data-stu-id="eab04-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="eab04-129">Расширенный стиль окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="eab04-130">Дополнительные сведения см. в разделе [**операторе EXSTYLE**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="eab04-131">**Шрифт** *PointSize*, *гарнитура*</span><span class="sxs-lookup"><span data-stu-id="eab04-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="eab04-132">Кегль и гарнитура шрифта.</span><span class="sxs-lookup"><span data-stu-id="eab04-132">Point size and typeface for the font.</span></span> <span data-ttu-id="eab04-133">Дополнительные сведения см. в разделе [**Font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="eab04-134">[](language-statement.md) *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="eab04-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="eab04-135">Язык диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-135">Language of the dialog box.</span></span> <span data-ttu-id="eab04-136">Дополнительные сведения см. в разделе [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="eab04-137"> *Menuname* меню</span><span class="sxs-lookup"><span data-stu-id="eab04-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="eab04-138">Используемое меню.</span><span class="sxs-lookup"><span data-stu-id="eab04-138">Menu to be used.</span></span> <span data-ttu-id="eab04-139">Это значение является либо именем меню, либо его целочисленным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="eab04-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="eab04-140">[](style-statement.md) *Стили* стилей</span><span class="sxs-lookup"><span data-stu-id="eab04-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="eab04-141">Стили диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-141">Styles of the dialog box.</span></span> <span data-ttu-id="eab04-142">Дополнительные сведения см. в разделе [**Style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="eab04-143">[**Версия**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="eab04-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="eab04-144">Определяемое пользователем значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eab04-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="eab04-145">Эта инструкция предназначена для использования дополнительными инструментами ресурсов и не используется системой.</span><span class="sxs-lookup"><span data-stu-id="eab04-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="eab04-146">Дополнительные сведения см. в разделе [**версия**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="eab04-147">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eab04-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="eab04-148">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="eab04-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eab04-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eab04-149">Remarks</span></span>

<span data-ttu-id="eab04-150">Функция [**жетдиалогбасеунитс**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) Возвращает базовые единицы диалогового окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="eab04-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="eab04-151">Точное значение координат зависит от стиля, определенного в выражении параметра [**Style**](style-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="eab04-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="eab04-152">Для диалоговых окон дочернего стиля координаты задаются относительно происхождения родительского окна, если только диалоговое окно не имеет стиль **DS \_ абсалигн**; в этом случае координаты отсчитываются относительно начала экрана отображения.</span><span class="sxs-lookup"><span data-stu-id="eab04-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="eab04-153">Не используйте стиль **\_ дочерний элемент WS** с модальным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="eab04-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="eab04-154">Функция [**диалогбокс**](/windows/win32/api/winuser/nf-winuser-dialogboxa) всегда отключает родителя или владельца только что созданного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="eab04-155">Если родительское окно отключено, его дочерние окна неявно отключаются.</span><span class="sxs-lookup"><span data-stu-id="eab04-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="eab04-156">Так как родительское окно диалогового окна дочернего стиля отключено, диалоговое окно дочернего стиля также имеет значение.</span><span class="sxs-lookup"><span data-stu-id="eab04-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="eab04-157">Если диалоговое окно имеет стиль **\_ Абсалигн в DS** , координаты его левого верхнего угла задаются относительно начала экрана, а не верхнего левого угла родительского окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="eab04-158">Этот стиль обычно используется, когда требуется, чтобы диалоговое окно запускалось в определенной части экрана независимо от того, где на экране может находиться родительское окно.</span><span class="sxs-lookup"><span data-stu-id="eab04-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="eab04-159">**Диалоговое окно** имя также можно использовать в качестве параметра class-name функции [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания окна с атрибутами диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab04-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="eab04-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="eab04-160">Examples</span></span>

<span data-ttu-id="eab04-161">Ниже показано использование инструкции **DIALOG** .</span><span class="sxs-lookup"><span data-stu-id="eab04-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="eab04-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eab04-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab04-163">Использование диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="eab04-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="eab04-164">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="eab04-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="eab04-165">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="eab04-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="eab04-166">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="eab04-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="eab04-167">**креатедиалог**</span><span class="sxs-lookup"><span data-stu-id="eab04-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="eab04-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="eab04-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="eab04-169">**диалогбокс**</span><span class="sxs-lookup"><span data-stu-id="eab04-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="eab04-170">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="eab04-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="eab04-171">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="eab04-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="eab04-172">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="eab04-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="eab04-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="eab04-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="eab04-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="eab04-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="eab04-175">**Версия**</span><span class="sxs-lookup"><span data-stu-id="eab04-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
