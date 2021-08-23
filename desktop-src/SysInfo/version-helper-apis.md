---
description: следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windowsным или Windows сервером.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Вспомогательные функции версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7156070e9c793e537d976c82a632142e04cd6669b110b7d0b9fc8da95671b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884175"
---
# <a name="version-helper-functions"></a>Вспомогательные функции версии

следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windowsным или Windows сервером. Эти функции предоставляют простые тесты, в которых используется функция [верифиверсионинфо](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) и рекомендованное значение "больше или равно" для сравнений, проверенных как надежные средства для определения версии операционной системы.

> [!Note]  
> эти api-интерфейсы определяются **версионхелперс. h**, который входит в состав пакета средств разработки программного обеспечения (SDK) для Windows 8.1. этот файл можно использовать с другими выпусками Microsoft Visual Studio для реализации тех же функций для Windows версий до Windows 8.1.

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
<td>указывает, совпадает ли текущая версия ос с версией Windows XP или больше нее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows XP с пакетом обновления 1 (SP1) или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows XP с пакетом обновления 2 (SP2) или больше.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows XP с пакетом обновления 3 (SP3) или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>исвиндовсвистаоргреатер</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows Vista или больше нее.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows Vista с пакетом обновления 1 (SP1) или больше.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows Vista с пакетом обновления 2 (SP2) или больше.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows 7 или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows 7 с пакетом обновления 1 (SP1) или больше.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows 8 или больше нее.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows 8.1 или больше нее.<br/> для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел compatibility, содержащий идентификаторы guid, указывающие Windows 8.1 и (или) Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>указывает, совпадает ли текущая версия ос с версией Windows 10 или больше нее.<br/> для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел compatibility, содержащий идентификатор GUID, обозначающий Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>исвиндовссервер</strong></a></td>
<td>указывает, является ли текущая ос выпуском Windows Server. приложения, которым необходимо различать версии сервера и клиента Windows должны вызывать эту функцию.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>исвиндовсверсионоргреатер</strong></a></td>
<td>
<blockquote>Эту функцию следует использовать только в том случае, если другие предоставляемые вспомогательные функции версий не соответствуют вашему сценарию.</blockquote>
<br/>Указывает, совпадает ли текущая версия ОС с предоставленными сведениями о версии или больше. эта функция полезна при подтверждении версии Windows Server, не имеющей номера версии с выпуском клиента.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Пример

Встроенные функции, определенные в файле заголовка **версионхелперс. h** , позволяют проверить версию операционной системы, возвращая **логическое** значение при проверке версии Windows.

например, если приложению требуется Windows 8 или более поздней версии, используйте следующий тест.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Связанные темы

- [осверсионинфоекс](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
