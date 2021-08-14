---
title: E (меню и другие ресурсы)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f2423b002afe055c425978a643753e029d817eee5e7eccfc4379d2410f88ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461254"
---
# <a name="e-menus-and-other-resources"></a>E (меню и другие ресурсы)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G р [. J K](i.md) L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Пустые меню запрещены**
</dt> <dd>

Ключевое слово **End** появляется перед тем, как все пункты меню определены в инструкции [**меню**](menu-resource.md) . пустые меню не разрешены компилятором ресурсов Microsoft Windows 32 (RC). Убедитесь, что в операторе **меню** отсутствуют открывающие кавычки.

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Ожидается END в диалоговом окне**
</dt> <dd>

Ключевое слово **End** должно находиться в конце инструкции [**диалогового окна**](dialog-resource.md) . Убедитесь, что в предыдущем операторе не осталось открывающих кавычек.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**КОНЕЦ ожидаемого в меню**
</dt> <dd>

Ключевое слово **End** должно находиться в конце инструкции [**меню**](menu-resource.md) . Убедитесь, что отсутствуют несовпадающие операторы **Begin** и **End** .

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Ошибка Креатингресаурце — имя**
</dt> <dd>

компилятору ресурсов Microsoft Windows 32 (RC) не удалось создать указанный двоичный ресурс (. RES). Убедитесь, что он не создается на диске только для чтения. Используйте параметр **/v** , чтобы узнать, создается ли файл.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Ожидается запятая в таблице сочетаний клавиш**
</dt> <dd>

для компилятора ресурсов Microsoft Windows 32 (RC) требуется запятая между параметрами *события* и *idvalue* в операторе [**ускорителей**](accelerators-resource.md) .

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Ожидаемое имя класса элемента управления**
</dt> <dd>

Параметр *Class* оператора [**Control**](control-control.md) в операторе [**DIALOG**](dialog-resource.md) должен быть одним из следующих типов элементов управления: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** или defined, определяемый пользователем. Убедитесь, что класс написан правильно.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Ожидаемое имя начертания шрифта**
</dt> <dd>

Параметр *гарнитуры* в операторе **Font** в [**диалоговом окне**](dialog-resource.md) должен быть символьной строкой, заключенной в двойные кавычки ("). Этот параметр задает имя шрифта.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Ожидаемое значение идентификатора для MenuItem**
</dt> <dd>

Оператор [**меню**](menu-resource.md) должен содержать инструкцию [**MenuItem**](menuitem-statement.md) , которая содержит либо целое число, либо символьную константу в параметре *менуид* .

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Ожидается строка меню**
</dt> <dd>

Каждая инструкция [**MenuItem**](menuitem-statement.md) и [**Popup**](popup-resource.md) должна содержать *текстовый* параметр. Этот параметр представляет собой строку, заключенную в двойные кавычки ("), которая указывает имя пункта меню или всплывающего меню. Для инструкции- **разделителя MenuItem** не требуется строка в кавычках.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Ожидаемое числовое значение команды**
</dt> <dd>

компилятор ресурсов Microsoft Windows (RC) ожидал числовой параметр *idvalue* в операторе [**ускорителей**](accelerators-resource.md) . Убедитесь, что вы использовали оператор [**\# define**](-define.md) для указания значения и что используемая константа написана правильно.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Ожидалась числовая константа в таблице строк**
</dt> <dd>

Числовая константа, определенная в инструкции [**\# define**](-define.md) , должна следовать непосредственно за ключевым словом **Begin** в операторе [**STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Ожидался размер числовой точки**
</dt> <dd>

Параметр *PointSize* инструкции [**Font**](font-statement.md) в [**диалоговом окне**](dialog-resource.md) должен иметь целочисленное значение размера точки.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Ожидаемая числовая константа диалогового окна**
</dt> <dd>

Для оператора [**диалогового окна**](dialog-resource.md) требуются целочисленные значения для параметров *x*, *y*, *Width* и *Height* . Убедитесь, что эти значения, которые включены после ключевого слова **DIALOG** , не являются отрицательными.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Ожидалась строка в STRINGTABLE**
</dt> <dd>

После каждого числового параметра *stringid* в операторе [**STRINGTABLE**](stringtable-resource.md) ожидается строка.

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Требуется строка или константа в качестве команды сочетания клавиш**
</dt> <dd>

компилятору ресурсов Microsoft Windows не удалось определить, какой ключ был настроен для ускорителя. Параметр *события* в операторе [**ускорителей**](accelerators-resource.md) может быть недопустимым.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Ожидаемое значение, блок или ключевое слово END.**
</dt> <dd>

Для структуры [**versionInfo**](versioninfo-resource.md) требуется ключевое слово **value**, **Block** или **End** .

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Ожидается номер для идентификатора**
</dt> <dd>

Для параметра *ID* инструкции [**Control**](control-control.md) в инструкции [**DIALOG**](dialog-resource.md) ожидается число. Убедитесь, что у вас есть число или оператор [**\# define**](-define.md) для идентификатора элемента управления.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Ожидается строка в кавычках для ключа**
</dt> <dd>

Ключевая строка, следующая за ключевым словом **Block** или **value** , должна быть заключена в двойные кавычки.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Ожидается строка в кавычках в классе диалогового окна**
</dt> <dd>

Параметр *класса* инструкции [**класса**](class-statement.md) в инструкции [**DIALOG**](dialog-resource.md) должен быть целым числом или строкой, заключенной в двойные кавычки (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Ожидается строка в кавычках в заголовке диалогового окна**
</dt> <dd>

Параметр *каптионтекст* инструкции [**Caption**](caption-statement.md) в инструкции [**DIALOG**](dialog-resource.md) должен быть символьной строкой, заключенной в двойные кавычки (").

</dd> </dl>

 

 




