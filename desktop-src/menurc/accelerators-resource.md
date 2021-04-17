---
title: Ресурс УСКОРИТЕЛей
description: Определяет один или несколько ускорителей для приложения. Сочетание клавиш — это клавиша, определяемая приложением, чтобы дать пользователю быстрый способ выполнения задачи.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Меню ресурсов УСКОРИТЕЛей и другие ресурсы
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533137"
---
# <a name="accelerators-resource"></a><span data-ttu-id="048f3-105">Ресурс УСКОРИТЕЛей</span><span class="sxs-lookup"><span data-stu-id="048f3-105">ACCELERATORS resource</span></span>

<span data-ttu-id="048f3-106">Определяет один или несколько ускорителей для приложения.</span><span class="sxs-lookup"><span data-stu-id="048f3-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="048f3-107">Сочетание клавиш — это клавиша, определяемая приложением, чтобы дать пользователю быстрый способ выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="048f3-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="048f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="048f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="048f3-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*акктабленаме*</span><span class="sxs-lookup"><span data-stu-id="048f3-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-110">Уникальное имя или 16-битовое целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="048f3-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="048f3-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="048f3-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-112">Ноль или более следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="048f3-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="048f3-113">Инструкция</span><span class="sxs-lookup"><span data-stu-id="048f3-113">Statement</span></span>                                                        | <span data-ttu-id="048f3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="048f3-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="048f3-115">[**Параметры**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="048f3-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="048f3-116">Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="048f3-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="048f3-117">Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="048f3-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="048f3-118">[](language-statement.md) *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="048f3-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="048f3-119">Указывает язык ресурса.</span><span class="sxs-lookup"><span data-stu-id="048f3-119">Specifies the language for the resource.</span></span> <span data-ttu-id="048f3-120">Дополнительные сведения см. в разделе [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="048f3-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="048f3-121">[**Версия**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="048f3-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="048f3-122">Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="048f3-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="048f3-123">Дополнительные сведения см. в разделе [**версия**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="048f3-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="048f3-124"><span id="event"></span><span id="EVENT"></span>*журнале*</span><span class="sxs-lookup"><span data-stu-id="048f3-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-125">Клавиша, используемая в качестве ускорителя.</span><span class="sxs-lookup"><span data-stu-id="048f3-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="048f3-126">Это может быть любой из следующих типов символов.</span><span class="sxs-lookup"><span data-stu-id="048f3-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="048f3-127">Тип</span><span class="sxs-lookup"><span data-stu-id="048f3-127">Type</span></span>                    | <span data-ttu-id="048f3-128">Описание</span><span class="sxs-lookup"><span data-stu-id="048f3-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="048f3-129">"*char*"</span><span class="sxs-lookup"><span data-stu-id="048f3-129">"*char*"</span></span>                | <span data-ttu-id="048f3-130">Одиночный символ, заключенный в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="048f3-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="048f3-131">Символу может предшествовать знак крышки (^), что означает, что символ является управляющим символом.</span><span class="sxs-lookup"><span data-stu-id="048f3-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="048f3-132">*Знак*</span><span class="sxs-lookup"><span data-stu-id="048f3-132">*Character*</span></span>             | <span data-ttu-id="048f3-133">Целочисленное значение, представляющее символ.</span><span class="sxs-lookup"><span data-stu-id="048f3-133">An integer value representing a character.</span></span> <span data-ttu-id="048f3-134">Параметр *типа* должен быть **ASCII**.</span><span class="sxs-lookup"><span data-stu-id="048f3-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="048f3-135">*символ виртуальной клавиши*</span><span class="sxs-lookup"><span data-stu-id="048f3-135">*virtual-key character*</span></span> | <span data-ttu-id="048f3-136">Целочисленное значение, представляющее виртуальный ключ.</span><span class="sxs-lookup"><span data-stu-id="048f3-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="048f3-137">Виртуальный ключ для буквенно-цифровых ключей можно указать, поместив прописную букву или цифру в двойные кавычки (например, "9" или "C").</span><span class="sxs-lookup"><span data-stu-id="048f3-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="048f3-138">Параметр *типа* должен быть **VIRTKEY**.</span><span class="sxs-lookup"><span data-stu-id="048f3-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="048f3-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span><span class="sxs-lookup"><span data-stu-id="048f3-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-140">16-битовое целочисленное значение без знака, идентифицирующее ускоритель.</span><span class="sxs-lookup"><span data-stu-id="048f3-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="048f3-141"><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="048f3-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-142">Требуется только в том случае, если параметр *события* является *символом* или *виртуальным ключом*.</span><span class="sxs-lookup"><span data-stu-id="048f3-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="048f3-143">Параметр *типа* указывает либо **ASCII** , либо **VIRTKEY**; Целочисленное значение *события* интерпретируется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="048f3-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="048f3-144">Если **VIRTKEY** указан, а *событие* содержит строку, *событие* должно быть в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="048f3-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="048f3-145"><span id="options"></span><span id="OPTIONS"></span>*Параметры*</span><span class="sxs-lookup"><span data-stu-id="048f3-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="048f3-146">параметры, определяющие ускоритель.</span><span class="sxs-lookup"><span data-stu-id="048f3-146">options that define the accelerator.</span></span> <span data-ttu-id="048f3-147">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="048f3-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="048f3-148">Параметр</span><span class="sxs-lookup"><span data-stu-id="048f3-148">Option</span></span>                             | <span data-ttu-id="048f3-149">Описание</span><span class="sxs-lookup"><span data-stu-id="048f3-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="048f3-150">**ИНВЕРТИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="048f3-150">**NOINVERT**</span></span>                       | <span data-ttu-id="048f3-151">Указывает, что при использовании сочетания клавиш не выделяется ни один элемент меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="048f3-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="048f3-152">Это полезно при определении ускорителей для таких действий, как прокрутка, которая не соответствует пункту меню.</span><span class="sxs-lookup"><span data-stu-id="048f3-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="048f3-153">Если параметр **инвертирует** не задан, то при использовании сочетания клавиш будет выделена команда меню верхнего уровня (если возможно).</span><span class="sxs-lookup"><span data-stu-id="048f3-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="048f3-154">Этот атрибут устарел и хранится только для обеспечения обратной совместимости с файлами ресурсов, предназначенными для 16-разрядных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="048f3-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="048f3-155">**МЕЩАЮЩИЙ**</span><span class="sxs-lookup"><span data-stu-id="048f3-155">**ALT**</span></span>                            | <span data-ttu-id="048f3-156">Вызывает активацию ускорителя только в том случае, если нажата клавиша ALT.</span><span class="sxs-lookup"><span data-stu-id="048f3-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="048f3-157">Применяется только к виртуальным ключам.</span><span class="sxs-lookup"><span data-stu-id="048f3-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="048f3-158">**МЕСТИ**</span><span class="sxs-lookup"><span data-stu-id="048f3-158">**SHIFT**</span></span>                          | <span data-ttu-id="048f3-159">Вызывает активацию ускорителя только в том случае, если нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="048f3-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="048f3-160">Применимо только к виртуальным ключам</span><span class="sxs-lookup"><span data-stu-id="048f3-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="048f3-161">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="048f3-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="048f3-162">Определяет символ как управляющий символ (ускоритель активируется только в том случае, если ключ элемента управления не работает).</span><span class="sxs-lookup"><span data-stu-id="048f3-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="048f3-163">Это действует так же, как использование курсора (^) перед символом ускорителя в параметре *события* .</span><span class="sxs-lookup"><span data-stu-id="048f3-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="048f3-164">Применимо только к виртуальным ключам</span><span class="sxs-lookup"><span data-stu-id="048f3-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="048f3-165">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="048f3-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="048f3-166">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="048f3-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="048f3-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="048f3-167">Remarks</span></span>

<span data-ttu-id="048f3-168">Функция [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) используется для преобразования сообщений ускорителя из очереди приложения в [**\_ команду WM**](./wm-command.md) или в сообщения [**\_ сискомманд WM**](./wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="048f3-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="048f3-169">Примеры</span><span class="sxs-lookup"><span data-stu-id="048f3-169">Examples</span></span>

<span data-ttu-id="048f3-170">В следующем примере демонстрируется использование сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="048f3-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="048f3-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="048f3-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="048f3-172">Использование сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="048f3-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="048f3-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="048f3-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="048f3-174">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="048f3-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="048f3-175">**Откроется**</span><span class="sxs-lookup"><span data-stu-id="048f3-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="048f3-176">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="048f3-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="048f3-177">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="048f3-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="048f3-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="048f3-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="048f3-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="048f3-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="048f3-180">**Версия**</span><span class="sxs-lookup"><span data-stu-id="048f3-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 