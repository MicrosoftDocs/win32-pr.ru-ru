---
title: Структура ПОПУПМЕНУИТЕМ
description: Содержит сведения о пунктах меню в ресурсе меню, открывающем меню или подменю. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Меню структуры ПОПУПМЕНУИТЕМ и другие ресурсы
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988329"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="d199a-105">Структура ПОПУПМЕНУИТЕМ</span><span class="sxs-lookup"><span data-stu-id="d199a-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="d199a-106">Содержит сведения о пунктах меню в ресурсе меню, открывающем меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="d199a-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="d199a-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="d199a-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d199a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d199a-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="d199a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d199a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d199a-110">**type**</span><span class="sxs-lookup"><span data-stu-id="d199a-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="d199a-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d199a-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d199a-112">Описывает пункт меню.</span><span class="sxs-lookup"><span data-stu-id="d199a-112">Describes the menu item.</span></span> <span data-ttu-id="d199a-113">Некоторые из значений, которые может включить этот элемент, перечислены в списке ниже.</span><span class="sxs-lookup"><span data-stu-id="d199a-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="d199a-114">В дополнение к показанным значениям этот элемент также может быть сочетанием значений типа, перечисленных с помощью члена **fType** структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="d199a-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="d199a-115">Это значения типа, которые начинаются с MFT \_ .</span><span class="sxs-lookup"><span data-stu-id="d199a-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="d199a-116">Чтобы использовать эти предопределенные \_ \* значения типа MFT, включите в RC-файл следующую инструкцию:</span><span class="sxs-lookup"><span data-stu-id="d199a-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="d199a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d199a-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="d199a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d199a-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="d199a-119"><dt>**MF \_ КОНЕЦ**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="d199a-120">Пункт меню является последним в меню; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="d199a-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="d199a-121"><dt>**MF \_ Всплывающее окно**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="d199a-122">Элемент меню открывает меню или подменю; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="d199a-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="d199a-123">**state**</span><span class="sxs-lookup"><span data-stu-id="d199a-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="d199a-124">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d199a-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d199a-125">Описывает пункт меню.</span><span class="sxs-lookup"><span data-stu-id="d199a-125">Describes the menu item.</span></span> <span data-ttu-id="d199a-126">Этот элемент может быть сочетанием значений состояния, перечисленных с элементом **двстате** структуры [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="d199a-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="d199a-127">Значения состояния — это те, которые начинаются с MFA \_ .</span><span class="sxs-lookup"><span data-stu-id="d199a-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="d199a-128">Чтобы использовать эти предопределенные \_ \* значения состояния MFA, включите в RC-файл следующую инструкцию:</span><span class="sxs-lookup"><span data-stu-id="d199a-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="d199a-129">**id**</span><span class="sxs-lookup"><span data-stu-id="d199a-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="d199a-130">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d199a-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d199a-131">Числовое выражение, идентифицирующее пункт меню, который передается [**в \_ командном сообщении WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="d199a-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="d199a-132">**Resinfo:**</span><span class="sxs-lookup"><span data-stu-id="d199a-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d199a-133">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d199a-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d199a-134">Набор битовых флагов, указывающих тип пункта меню.</span><span class="sxs-lookup"><span data-stu-id="d199a-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="d199a-135">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d199a-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="d199a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d199a-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="d199a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d199a-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="d199a-138"><dt>**МФР \_ КОНЕЦ**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="d199a-139">Элемент меню является последним в этом подменю или ресурсе меню; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="d199a-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="d199a-140"><dt>**МФР \_ Всплывающее окно**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="d199a-141">Элемент меню открывает меню или подменю; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="d199a-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="d199a-142">**менутекст**</span><span class="sxs-lookup"><span data-stu-id="d199a-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="d199a-143">Тип: **сзорорд**</span><span class="sxs-lookup"><span data-stu-id="d199a-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="d199a-144">Строка в Юникоде, заканчивающаяся нулем и содержащая текст для данного элемента меню.</span><span class="sxs-lookup"><span data-stu-id="d199a-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="d199a-145">Фиксированного ограничения на размер этой строки не существует.</span><span class="sxs-lookup"><span data-stu-id="d199a-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d199a-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d199a-146">Remarks</span></span>

<span data-ttu-id="d199a-147">Для каждого пункта меню, открывающего меню или подменю, существует одна структура **попупменуитем** .</span><span class="sxs-lookup"><span data-stu-id="d199a-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="d199a-148">Укажите этот тип пункта меню, установив для члена **типа** значение **MF и \_** установив бит **\_ всплывающего окна МФР** в элементе **Resinfo:** в значение 0x0001.</span><span class="sxs-lookup"><span data-stu-id="d199a-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="d199a-149">В этом случае окончательные данные, записанные в [**ресурс \_ меню RT**](/windows/desktop/menurc/resource-types) для меню или подменю, являются структурой [**менухелпид**](menuhelpid.md) .</span><span class="sxs-lookup"><span data-stu-id="d199a-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="d199a-150">**Менухелпид** содержит числовое выражение, идентифицирующее меню во время обработки [**\_ справки WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="d199a-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="d199a-151">Кроме того, после каждой структуры **попупменуитем** , имеющей бит **\_ всплывающего окна МФР** в элементе **Resinfo:** , будет следовать структура [**менухелпид**](menuhelpid.md) плюс дополнительное число структур **попупменуитем** , по одному для каждого пункта меню в этом подменю.</span><span class="sxs-lookup"><span data-stu-id="d199a-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="d199a-152">Последняя структура **попупменуитем** в подменю будет иметь бит **\_ конца МФР** , установленный в элементе **Resinfo:** .</span><span class="sxs-lookup"><span data-stu-id="d199a-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="d199a-153">Чтобы найти конец ресурса, найдите соответствующий **МФР \_ конец** для каждого **\_ всплывающего окна МФР** и еще одну дополнительную **мфрную часть \_** , соответствующую самому внешнему набору пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="d199a-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="d199a-154">Укажите последний элемент меню, задав для члена **типа** значение **MF \_ End**.</span><span class="sxs-lookup"><span data-stu-id="d199a-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="d199a-155">Так как вложенные меню можно вкладывать, можно использовать несколько уровней в **MF \_**.</span><span class="sxs-lookup"><span data-stu-id="d199a-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="d199a-156">В этих случаях пункты меню являются последовательными.</span><span class="sxs-lookup"><span data-stu-id="d199a-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="d199a-157">Требования</span><span class="sxs-lookup"><span data-stu-id="d199a-157">Requirements</span></span>



| <span data-ttu-id="d199a-158">Требование</span><span class="sxs-lookup"><span data-stu-id="d199a-158">Requirement</span></span> | <span data-ttu-id="d199a-159">Значение</span><span class="sxs-lookup"><span data-stu-id="d199a-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d199a-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d199a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d199a-161">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d199a-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d199a-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d199a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d199a-163">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d199a-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d199a-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d199a-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="d199a-165">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d199a-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d199a-166">**менухеадер**</span><span class="sxs-lookup"><span data-stu-id="d199a-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="d199a-167">**менухелпид**</span><span class="sxs-lookup"><span data-stu-id="d199a-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="d199a-168">**ОБЪЕКТАМИ MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="d199a-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="d199a-169">**нормалменуитем**</span><span class="sxs-lookup"><span data-stu-id="d199a-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="d199a-170">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d199a-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d199a-171">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="d199a-171">Resources</span></span>](resources.md)
</dt> </dl>

 

