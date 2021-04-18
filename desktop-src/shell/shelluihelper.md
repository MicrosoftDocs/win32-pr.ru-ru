---
description: Реализовано оболочкой, чтобы помочь сценариям и разработчикам Microsoft Visual Basic использовать некоторые функции, доступные в оболочке. Объект Шеллуихелпер не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.
title: Объект Шеллуихелпер (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986020"
---
# <a name="shelluihelper-object"></a>Объект Шеллуихелпер

Реализовано оболочкой, чтобы помочь сценариям и разработчикам Microsoft Visual Basic использовать некоторые функции, доступные в оболочке. Объект **шеллуихелпер** не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.

## <a name="members"></a>Элементы

Объект **шеллуихелпер** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Объект **шеллуихелпер** содержит эти методы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Метод</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>аддчаннел</strong></a></td>
<td style="text-align: left;">Добавляет новый канал в список каналов в меню <strong>Избранное</strong> Internet Explorer и на панель <strong>каналов</strong> на рабочем столе.<br/>
<blockquote>
[!Note]<br />
Этот метод больше не поддерживается в Windows Vista. В этой операционной системе возвращается E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>адддесктопкомпонент</strong></a></td>
<td style="text-align: left;">Добавляет элемент в активный рабочий стол.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>аддфаворите</strong></a></td>
<td style="text-align: left;">Отображает пользовательский интерфейс по умолчанию для создания элемента избранного. Пользовательский интерфейс инициализируется с указанными параметрами.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Указывает, подписан ли указанный URL-адрес на.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




