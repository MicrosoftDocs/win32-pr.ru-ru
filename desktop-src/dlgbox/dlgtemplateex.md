---
title: Структура ДЛГТЕМПЛАТИКС
description: Расширенный шаблон диалогового окна начинается с заголовка ДЛГТЕМПЛАТИКС, который описывает диалоговое окно и задает количество элементов управления в диалоговом окне.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Диалоговые окна структуры ДЛГТЕМПЛАТИКС
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534739"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="05f43-104">Структура ДЛГТЕМПЛАТИКС</span><span class="sxs-lookup"><span data-stu-id="05f43-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="05f43-105">Расширенный шаблон диалогового окна начинается с заголовка **длгтемплатикс** , который описывает диалоговое окно и задает количество элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="05f43-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="05f43-106">Для каждого элемента управления в диалоговом окне Расширенный шаблон диалогового окна содержит блок данных, который использует формат [**длгитемтемплатикс**](dlgitemtemplateex.md) для описания элемента управления.</span><span class="sxs-lookup"><span data-stu-id="05f43-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="05f43-107">Структура **длгтемплатикс** не определена ни в одном из файлов стандартного заголовка.</span><span class="sxs-lookup"><span data-stu-id="05f43-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="05f43-108">Определение структуры приведено здесь, чтобы объяснить формат расширенного шаблона для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f43-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05f43-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="05f43-110">Члены</span><span class="sxs-lookup"><span data-stu-id="05f43-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="05f43-111">**длгвер**</span><span class="sxs-lookup"><span data-stu-id="05f43-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-112">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="05f43-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-113">Номер версии расширенного шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="05f43-114">Этот элемент должен иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="05f43-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-115">**подпись**</span><span class="sxs-lookup"><span data-stu-id="05f43-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-116">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="05f43-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-117">Указывает, является ли шаблон расширенным шаблоном диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="05f43-118">Если **сигнатура** имеет значение 0xFFFF, это расширенный шаблон диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="05f43-119">В этом случае член **длгвер** указывает номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="05f43-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="05f43-120">Если **сигнатура** имеет любое значение, отличное от 0xFFFF, это стандартный шаблон диалогового окна, в котором используются структуры [**длгтемплате**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) и [**длгитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="05f43-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-121">**Идентификатор справки**</span><span class="sxs-lookup"><span data-stu-id="05f43-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-122">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05f43-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-123">Идентификатор контекста справки для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="05f43-124">Когда система отправляет [**\_ справочное сообщение WM**](../shell/wm-help.md) , оно передает это значение в элемент **вконтекстид** структуры [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="05f43-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-125">**Операторе EXSTYLE**</span><span class="sxs-lookup"><span data-stu-id="05f43-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-126">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05f43-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-127">Расширенные стили Windows.</span><span class="sxs-lookup"><span data-stu-id="05f43-127">The extended windows styles.</span></span> <span data-ttu-id="05f43-128">Этот элемент не используется при создании диалоговых окон, но приложения, использующие шаблоны диалоговых окон, могут использовать его для создания других типов окон.</span><span class="sxs-lookup"><span data-stu-id="05f43-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="05f43-129">Список значений см. в разделе [**Расширенные стили окон**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="05f43-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="05f43-130">**style**</span><span class="sxs-lookup"><span data-stu-id="05f43-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-131">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05f43-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-132">Стиль диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-132">The style of the dialog box.</span></span> <span data-ttu-id="05f43-133">Этот элемент может быть сочетанием [значений стиля окна](/windows/desktop/winmsg/window-styles) и [значений стиля диалогового](dialog-box-styles.md)окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="05f43-134">Если **Style** включает в себя стиль диалогового окна **DS \_ сетфонт** или **DS \_ шеллфонт** , заголовок **длгтемплатикс** расширенного диалогового окна содержит четыре дополнительных элемента ( **PointSize**, **вес**, **курсив** и **гарнитура**), описывающие шрифт, используемый для текста в клиентской области и элементах управления диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="05f43-135">По возможности система создает шрифт в соответствии со значениями, указанными в этих элементах.</span><span class="sxs-lookup"><span data-stu-id="05f43-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="05f43-136">Затем система отправляет сообщение [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont) в диалоговое окно и каждый элемент управления для предоставления маркера для шрифта.</span><span class="sxs-lookup"><span data-stu-id="05f43-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="05f43-137">Дополнительные сведения см. в разделе [Шрифты диалогового окна](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="05f43-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="05f43-138">**кдлгитемс**</span><span class="sxs-lookup"><span data-stu-id="05f43-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-139">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="05f43-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-140">Число элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="05f43-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-141">**x**</span><span class="sxs-lookup"><span data-stu-id="05f43-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-142">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="05f43-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-143">Координата x в диалоговых окнах в левом верхнем углу диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-144">**y**</span><span class="sxs-lookup"><span data-stu-id="05f43-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-145">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="05f43-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-146">Координата по оси y в диалоговом окне единицы в левом верхнем углу диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-147">**/CX**</span><span class="sxs-lookup"><span data-stu-id="05f43-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-148">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="05f43-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-149">Ширина (в диалоговых окнах) диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-150">**CY**</span><span class="sxs-lookup"><span data-stu-id="05f43-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-151">Тип: **короткий**</span><span class="sxs-lookup"><span data-stu-id="05f43-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-152">Высота диалогового окна в единицах диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-153">**меню**</span><span class="sxs-lookup"><span data-stu-id="05f43-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-154">Тип: **SZ \_ или \_**</span><span class="sxs-lookup"><span data-stu-id="05f43-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-155">Массив из 16-разрядных элементов переменной длины, определяющий ресурс меню для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="05f43-156">Если первый элемент массива — Символ 0x0000, в диалоговом окне нет меню, а в массиве нет других элементов.</span><span class="sxs-lookup"><span data-stu-id="05f43-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="05f43-157">Если первый элемент имеет значение 0xFFFF, в массиве имеется один дополнительный элемент, указывающий порядковый номер ресурса меню в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="05f43-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="05f43-158">Если первый элемент имеет любое другое значение, система рассматривает массив как строку в Юникоде, заканчивающуюся нулем, которая указывает имя ресурса меню в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="05f43-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-159">**виндовкласс**</span><span class="sxs-lookup"><span data-stu-id="05f43-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-160">Тип: **SZ \_ или \_**</span><span class="sxs-lookup"><span data-stu-id="05f43-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-161">Массив из 16-разрядных элементов переменной длины, определяющий класс окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="05f43-162">Если первый элемент массива является символ 0x0000, система использует предопределенный класс диалогового окна для диалогового окна, а массив не имеет других элементов.</span><span class="sxs-lookup"><span data-stu-id="05f43-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="05f43-163">Если первый элемент имеет значение 0xFFFF, в массиве имеется один дополнительный элемент, указывающий порядковый номер предопределенного системного класса окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="05f43-164">Если первый элемент имеет любое другое значение, система рассматривает массив как строку в Юникоде, заканчивающуюся нулем, которая указывает имя зарегистрированного класса окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-165">**title**</span><span class="sxs-lookup"><span data-stu-id="05f43-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-166">Тип: **WCHAR \[ титлелен \]**</span><span class="sxs-lookup"><span data-stu-id="05f43-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-167">Название диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-167">The title of the dialog box.</span></span> <span data-ttu-id="05f43-168">Если первый элемент массива — Символ 0x0000, то диалоговое окно не имеет заголовка, а массив не содержит других элементов.</span><span class="sxs-lookup"><span data-stu-id="05f43-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-169">**PointSize**</span><span class="sxs-lookup"><span data-stu-id="05f43-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-170">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="05f43-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-171">Размер кегля шрифта, используемый для текста в диалоговом окне и его элементах управления.</span><span class="sxs-lookup"><span data-stu-id="05f43-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="05f43-172">Этот элемент доступен только в том случае, если элемент **Style** указывает **DS \_ сетфонт** или **DS \_ шеллфонт**.</span><span class="sxs-lookup"><span data-stu-id="05f43-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="05f43-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-174">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="05f43-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-175">Вес шрифта.</span><span class="sxs-lookup"><span data-stu-id="05f43-175">The weight of the font.</span></span> <span data-ttu-id="05f43-176">Обратите внимание, что, хотя это может быть любое из значений, перечисленных для элемента **лфвеигхт** структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , любое используемое значение будет автоматически изменено на « **\_ обычная нормальная**».</span><span class="sxs-lookup"><span data-stu-id="05f43-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="05f43-177">Этот элемент доступен только в том случае, если элемент **Style** указывает **DS \_ сетфонт** или **DS \_ шеллфонт**.</span><span class="sxs-lookup"><span data-stu-id="05f43-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-178">**курсив**</span><span class="sxs-lookup"><span data-stu-id="05f43-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-179">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="05f43-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-180">Указывает, является ли шрифт курсивом.</span><span class="sxs-lookup"><span data-stu-id="05f43-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="05f43-181">Если это значение равно **true**, шрифт будет курсивом.</span><span class="sxs-lookup"><span data-stu-id="05f43-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="05f43-182">Этот элемент доступен только в том случае, если элемент **Style** указывает **DS \_ сетфонт** или **DS \_ шеллфонт**.</span><span class="sxs-lookup"><span data-stu-id="05f43-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-183">**charset**</span><span class="sxs-lookup"><span data-stu-id="05f43-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-184">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="05f43-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-185">Используемая кодировка.</span><span class="sxs-lookup"><span data-stu-id="05f43-185">The character set to be used.</span></span> <span data-ttu-id="05f43-186">Дополнительные сведения см. в разделе **лфчарсет** элемента [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="05f43-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="05f43-187">Этот элемент доступен только в том случае, если элемент **Style** указывает **DS \_ сетфонт** или **DS \_ шеллфонт**.</span><span class="sxs-lookup"><span data-stu-id="05f43-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="05f43-188">**начертан**</span><span class="sxs-lookup"><span data-stu-id="05f43-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="05f43-189">Тип: **WCHAR \[ стринглен \]**</span><span class="sxs-lookup"><span data-stu-id="05f43-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="05f43-190">Имя гарнитуры шрифта.</span><span class="sxs-lookup"><span data-stu-id="05f43-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="05f43-191">Этот элемент доступен только в том случае, если элемент **Style** указывает **DS \_ сетфонт** или **DS \_ шеллфонт**.</span><span class="sxs-lookup"><span data-stu-id="05f43-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05f43-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05f43-192">Remarks</span></span>

<span data-ttu-id="05f43-193">Вы можете использовать расширенный шаблон диалогового окна вместо стандартного шаблона диалогового окна в функциях [**креатедиалогиндиректпарам**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**диалогбоксиндиректпарам**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**креатедиалогиндирект**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)и [**диалогбоксиндирект**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="05f43-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="05f43-194">Следующий заголовок **длгтемплатикс** в расширенном шаблоне диалогового окна — одна или несколько структур [**длгитемтемплатикс**](dlgitemtemplateex.md) , описывающих элементы управления диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05f43-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="05f43-195">Элемент **кдлгитемс** структуры **длгитемтемплатикс** указывает количество структур **длгитемтемплатикс** , которые следуют за шаблоном.</span><span class="sxs-lookup"><span data-stu-id="05f43-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="05f43-196">Каждая структура [**длгитемтемплатикс**](dlgitemtemplateex.md) в шаблоне должна быть согласована на границе **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="05f43-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="05f43-197">Если элемент **Style** указывает стиль **DS \_ сетфонт** или **DS \_ шеллфонт** , первая структура **длгитемтемплатикс** начинается с первой границы **DWORD** после строки **гарнитуры** .</span><span class="sxs-lookup"><span data-stu-id="05f43-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="05f43-198">Если эти стили не указаны, первая структура начинается с первой границы **DWORD** после строки **заголовка** .</span><span class="sxs-lookup"><span data-stu-id="05f43-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="05f43-199">Массивы **меню**, **виндовкласс**, **Title** и **гарнитуры** должны быть согласованы по границам **слов** .</span><span class="sxs-lookup"><span data-stu-id="05f43-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="05f43-200">При указании символьных строк в массивах **меню**, **виндовкласс**, **Title** и **гарнитуре** необходимо использовать строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="05f43-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="05f43-201">Используйте функцию [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) для создания этих строк Юникода из строк ANSI.</span><span class="sxs-lookup"><span data-stu-id="05f43-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="05f43-202">Члены **x**, **y**, **CX** и **CY** задают значения в диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="05f43-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="05f43-203">Эти значения можно преобразовать в единицы экрана (в пикселях) с помощью функции [**мапдиалогрект**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="05f43-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f43-204">Требования</span><span class="sxs-lookup"><span data-stu-id="05f43-204">Requirements</span></span>



| <span data-ttu-id="05f43-205">Требование</span><span class="sxs-lookup"><span data-stu-id="05f43-205">Requirement</span></span> | <span data-ttu-id="05f43-206">Значение</span><span class="sxs-lookup"><span data-stu-id="05f43-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="05f43-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05f43-207">Minimum supported client</span></span><br/> | <span data-ttu-id="05f43-208">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05f43-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="05f43-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05f43-209">Minimum supported server</span></span><br/> | <span data-ttu-id="05f43-210">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05f43-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="05f43-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05f43-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="05f43-212">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="05f43-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05f43-213">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="05f43-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="05f43-214">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="05f43-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="05f43-215">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="05f43-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="05f43-216">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="05f43-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="05f43-217">**длгитемтемплатикс**</span><span class="sxs-lookup"><span data-stu-id="05f43-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="05f43-218">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="05f43-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="05f43-219">**WM \_ сетфонт**</span><span class="sxs-lookup"><span data-stu-id="05f43-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="05f43-220">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="05f43-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05f43-221">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="05f43-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="05f43-222">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="05f43-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="05f43-223">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="05f43-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="05f43-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="05f43-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

