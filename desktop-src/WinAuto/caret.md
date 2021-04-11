---
title: Курсор (Справочник по элементам пользовательского интерфейса MSAA)
description: Курсор является мигающей линией, блоком или точечным рисунком в клиентской области окна или в элементе управления, который принимает ввод с клавиатуры.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103890179"
---
# <a name="caret-msaa-ui-element-reference"></a>Курсор (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются символы крышки для Справочника по элементам пользовательского интерфейса MSAA. Использование «крышки» в различных платформах пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Курсор является мигающей линией, блоком или точечным рисунком в клиентской области окна или в элементе управления, который принимает ввод с клавиатуры. Указывает место вставки текста или графики. Так как только одно окно во времени имеет фокус клавиатуры, в системе имеется только один курсор.

## <a name="iaccessible-methods"></a>Методы IAccessible

Курсор поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Курсор поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Комментарии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>Свойство <strong>ChildCount</strong> равно нулю.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></td>
<td>Свойство <strong>Name</strong> имеет значение &quot; Edit &quot; .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></td>
<td>Свойство <strong>Role</strong> имеет значение <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></td>
<td>Свойства <strong>State</strong> могут иметь следующие значения:
<ul>
<li>Ноль, что означает, что курсор является видимым</li>
<li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Примечания

-   В отличие от других элементов пользовательского интерфейса, у объекта курсора нет связанного с ним обработчика окна. Чтобы получить доступ к объекту курсора, клиенты должны задать [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и дождаться, пока объект курсора не выдаст события.
-   Объект курсора в элементе управления "форматированный текст", предоставляемый Riched20.dll (который используется в текстовых редакторах, таких как Microsoft WordPad в Windows 98), не отправляет никаких [виневентс](winevents-infrastructure.md) при изменении его позиции во время выбора текста. Когда пользователь нажимает клавишу SHIFT и клавиши со стрелками для выбора текста, объект курсора не активирует [**\_ объект события \_ локатиончанже**](event-constants.md) WinEvent. Аналогично, если выделение устанавливается программно с помощью многофункциональных сообщений редактирования, объект курсора не отправляет никаких событий для указания его новой позиции.

    Все приложения, использующие Riched20.dll, представляют эту проблему. Приложения, использующие более ранние версии элемента управления Rich Edit, правильно отправляют события на основе выбранных элементов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




