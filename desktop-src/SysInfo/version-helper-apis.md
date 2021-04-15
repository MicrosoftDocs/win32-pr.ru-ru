---
description: Следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windows или Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Вспомогательные функции версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "105669521"
---
# <a name="version-helper-functions"></a>Вспомогательные функции версии

Следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windows или Windows Server. Эти функции предоставляют простые тесты, в которых используется функция [верифиверсионинфо](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) и рекомендованное значение "больше или равно" для сравнений, проверенных как надежные средства для определения версии операционной системы.

> [!Note]  
> Эти API-интерфейсы определяются **версионхелперс. h**, который входит в состав пакета средств разработки программного обеспечения (SDK) для Windows 8.1. Этот файл можно использовать с другими выпусками Microsoft Visual Studio для реализации тех же функций для версий Windows, которые были выпущены до Windows 8.1.

<table>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>исвиндовскспоргреатер</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows XP или превышает ее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 1 (SP1) или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 2 (SP2) или больше нее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 3 (SP3) или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>исвиндовсвистаоргреатер</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows Vista или превышает ее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows Vista с пакетом обновления 1 (SP1) или больше.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows Vista с пакетом обновления 2 (SP2) или больше.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows 7 или превышает ее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows 7 с пакетом обновления 1 (SP1) или больше нее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows 8 или превышает ее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows 8.1 или больше нее.<br/> Для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел Compatibility, содержащий идентификаторы GUID, указывающие Windows 8.1 и (или) Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Указывает, совпадает ли текущая версия ОС с версией Windows 10 или превышает ее.<br/> Для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел Compatibility, содержащий идентификатор GUID, обозначающий Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>исвиндовссервер</strong></a></td>
<td>Указывает, является ли текущая ОС выпуском Windows Server. Приложения, которым необходимо различать серверные и клиентские версии Windows, должны вызывать эту функцию.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>исвиндовсверсионоргреатер</strong></a></td>
<td>
<blockquote>Эту функцию следует использовать только в том случае, если другие предоставляемые вспомогательные функции версий не соответствуют вашему сценарию.</blockquote>
<br/>Указывает, совпадает ли текущая версия ОС с предоставленными сведениями о версии или больше. Эта функция полезна при подтверждении версии Windows Server, которая не поддерживает общий номер версии с выпуском клиента.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Пример

Встроенные функции, определенные в файле заголовка **версионхелперс. h** , позволяют проверить версию операционной системы, возвращая **логическое** значение при тестировании для версии Windows.

Например, если приложению требуется Windows 8 или более поздней версии, используйте следующий тест.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>См. также

- [осверсионинфоекс](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
