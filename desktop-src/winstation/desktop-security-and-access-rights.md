---
title: Безопасность настольных систем и права доступа
description: Безопасность позволяет управлять доступом к объектам настольных систем. Дополнительные сведения о безопасности см. в разделе Модель Access-Control.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413284"
---
# <a name="desktop-security-and-access-rights"></a>Безопасность настольных систем и права доступа

Безопасность позволяет управлять доступом к объектам настольных систем. Дополнительные сведения о безопасности см. в разделе [модель управления доступом](/windows/desktop/SecAuthZ/access-control-model).

При вызове функции [**креатедесктоп**](/windows/win32/api/winuser/nf-winuser-createdesktopa) или [**креатедесктопекс**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) можно указать [дескриптор безопасности](/windows/desktop/SecAuthZ/security-descriptors) для объекта Desktop. Если указано значение NULL, Рабочий стол получает дескриптор безопасности по умолчанию. Списки ACL в дескрипторе безопасности рабочего стола по умолчанию поступают от его родительской станции.

Чтобы получить или задать дескриптор безопасности объекта Windows Station, вызовите функции [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

При вызове функции [**опендесктоп**](/windows/win32/api/winuser/nf-winuser-opendesktopa) или [**опенинпутдесктоп**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) система проверяет запрошенные права доступа к дескриптору безопасности объекта.

Допустимые права доступа для объектов рабочего стола включают [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) и некоторые права доступа для конкретного объекта. В следующей таблице перечислены стандартные права доступа, используемые всеми объектами.

| Значение                       | Значение                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Требуется для удаления объекта.                                                                                                                                                                                                                                                       |
| \_Управление чтением (0x00020000L) | Требуется для чтения сведений в дескрипторе безопасности объекта, не включая сведения из списка SACL. Для чтения или записи списка SACL необходимо запросить право доступа к \_ системе безопасности системы доступа \_ . Дополнительные сведения см. в статье [право доступа к SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| Синхронизация (0x00100000L)   | Не поддерживается для объектов настольных систем.                                                                                                                                                                                                                                                   |
| ЗАПИСЬ \_ DAC (0x00040000L)    | Требуется для изменения списка DACL в дескрипторе безопасности объекта.                                                                                                                                                                                                               |
| \_Владелец записи (0x00080000L)  | Требуется для изменения владельца в дескрипторе безопасности объекта.                                                                                                                                                                                                              |



 

В следующей таблице перечислены права доступа для конкретного объекта.



| Право доступа                       | Описание                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ креатемену (0x0004L)      | Требуется для создания меню на рабочем столе.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Требуется для создания окна на рабочем столе.                                                 |
| \_Перечисление Desktop (0x0040L)       | Требуется для перечисления рабочего стола.                                                  |
| DESKTOP \_ хукконтрол (0x0008L)     | Требуется для установки любого обработчика окна.                                              |
| DESKTOP \_ жаурналплайбакк (0x0020L) | Требуется для выполнения воспроизведения журнала на рабочем столе.                                          |
| DESKTOP \_ жаурналрекорд (0x0010L)   | Требуется для выполнения записи журнала на рабочем столе.                                         |
| DESKTOP \_ READOBJECTS (0x0001L)     | Требуется для чтения объектов на рабочем столе.                                                    |
| DESKTOP \_ свитчдесктоп (0x0100L)   | Требуется для активации рабочего стола с помощью функции [**свитчдесктоп**](/windows/win32/api/winuser/nf-winuser-switchdesktop) . |
| DESKTOP \_ вритеобжектс (0x0080L)    | Требуется для записи объектов на рабочем столе.                                                   |



 

Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для объекта Desktop, содержащегося в интерактивной рабочей станции сеанса входа пользователя.



<table>
<thead>
<tr class="header">
<th>Право доступа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

Можно запросить \_ право доступа к системе \_ безопасности системы доступа к объекту рабочего стола, если вы хотите прочитать или записать список SACL объекта. Дополнительные сведения см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [права доступа к спискам SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 