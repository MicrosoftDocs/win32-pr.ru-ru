---
title: Права доступа и безопасность оконной станции
description: Безопасность позволяет управлять доступом к объектам Windows Station. Дополнительные сведения о безопасности см. в разделе Модель Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710291"
---
# <a name="window-station-security-and-access-rights"></a>Права доступа и безопасность оконной станции

Безопасность позволяет управлять доступом к объектам Windows Station. Дополнительные сведения о безопасности см. в разделе [модель управления доступом](/windows/desktop/SecAuthZ/access-control-model).

При вызове функции [**креатевиндовстатион**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) можно указать [дескриптор безопасности](/windows/desktop/SecAuthZ/security-descriptors) для объекта Windows Station. При указании значения NULL станция окна получает дескриптор безопасности по умолчанию. Списки ACL в дескрипторе безопасности по умолчанию для станции Windows поступают из основного маркера или токена олицетворения создателя.

Чтобы получить или задать дескриптор безопасности объекта Windows Station, вызовите функции [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

При вызове функции [**опенвиндовстатион**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) система проверяет запрошенные права доступа к дескриптору безопасности объекта.

Допустимые права доступа для объектов Windows Station включают [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) и некоторые права доступа для конкретного объекта. В следующей таблице перечислены стандартные права доступа, используемые всеми объектами.

| Значение                       | Значение                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Требуется для удаления объекта.                                                                                                                                                                                                                                                       |
| \_Управление чтением (0x00020000L) | Требуется для чтения сведений в дескрипторе безопасности объекта, не включая сведения из списка SACL. Для чтения или записи списка SACL необходимо запросить право доступа к \_ системе безопасности системы доступа \_ . Дополнительные сведения см. в статье [право доступа к SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| Синхронизация (0x00100000L)   | Не поддерживается для объектов оконной станции.                                                                                                                                                                                                                                            |
| ЗАПИСЬ \_ DAC (0x00040000L)    | Требуется для изменения списка DACL в дескрипторе безопасности объекта.                                                                                                                                                                                                               |
| \_Владелец записи (0x00080000L)  | Требуется для изменения владельца в дескрипторе безопасности объекта.                                                                                                                                                                                                              |



 

В следующей таблице перечислены права доступа для конкретного объекта.



| Право доступа                        | Описание                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ВИНСТА \_ все \_ доступ (0x37F)         | Все возможные права доступа для станции Windows.                                                                                                                                                                                                                            |
| ВИНСТА \_ акцессклипбоард (0x0004L)   | Требуется для использования буфера обмена.                                                                                                                                                                                                                                                |
| ВИНСТА \_ акцессглобалатомс (0x0020L) | Требуется для управления глобальными атомами.                                                                                                                                                                                                                                          |
| ВИНСТА \_ креатедесктоп (0x0008L)     | Требуется для создания новых объектов рабочего стола на станции Windows.                                                                                                                                                                                                                 |
| ВИНСТА \_ енумдесктопс (0x0001L)      | Требуется для перечисления существующих объектов Desktop.                                                                                                                                                                                                                               |
| \_Перечисление винста (0x0100L)         | Требуется для перечисления станции окон.                                                                                                                                                                                                                             |
| ВИНСТА \_ екситвиндовс (0x0040L)       | Требуется для успешного вызова функции [**екситвиндовс**](/windows/desktop/api/winuser/nf-winuser-exitwindows) или [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) . Windows-станции могут совместно использоваться пользователями, а этот тип доступа может препятствовать выходу из системы владельца Windows-станции другими пользователями. |
| ВИНСТА \_ реадаттрибутес (0x0002L)    | Требуется для чтения атрибутов объекта Windows Station. Этот атрибут включает параметры цвета и другие глобальные свойства Windows Station.                                                                                                                                |
| ВИНСТА \_ реадскрин (0x0200L)        | Требуется для доступа к содержимому экрана.                                                                                                                                                                                                                                           |
| ВИНСТА \_ вритеаттрибутес (0x0010L)   | Требуется для изменения атрибутов объекта Windows Station. Атрибуты включают параметры цвета и другие глобальные свойства Windows Station.                                                                                                                               |



 

Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для объекта интерактивной рабочей станции, который является станцией окна, назначенной сеансу входа текущего пользователя.



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для неинтерактивного объекта Windows Station. Система назначает неинтерактивные станции окон всем сеансам входа, кроме текущего пользователя.



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Вы можете запросить право доступа к \_ системе безопасности системы доступа \_ к объекту Windows Station, если хотите прочитать или записать список SACL объекта. Дополнительные сведения см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [права доступа к спискам SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 