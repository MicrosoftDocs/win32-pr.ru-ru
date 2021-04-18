---
description: Локализованные версии таблицы ошибок и таблицы Актионтекст предоставляются пакетом SDK для установщик Windows. Версии этих таблиц с ошибками и Актионте. для французского языка находятся в папке Intl пакета SDK установщик Windows.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Импорт локализованных таблиц ошибок и Актионтекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650970"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Импорт локализованных таблиц ошибок и Актионтекст

Локализованные версии [таблицы ошибок](error-table.md) и [таблицы актионтекст](actiontext-table.md) предоставляются пакетом SDK для установщик Windows. Версии этих таблиц с ошибками и Актионте. для французского языка находятся в папке Intl пакета SDK установщик Windows.

Вы можете использовать редактор таблиц Orca или служебную программу Msidb.exe, поставляемую с пакетом SDK, для импорта французских версий этих таблиц в базу данных.

Пример использования [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) и [**метода Import**](database-import.md) [**объекта базы данных**](database-object.md) предоставляется в пакете SDK установщик Windows в качестве служебной WiImport.vbs. В следующем фрагменте кода, Imp.vbs, также иллюстрируется использование метода Import и предназначено для использования с сервером сценариев Windows.


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



Чтобы импортировать и заменить таблицу ошибок с ошибкой. параметром, можно использовать командную строку, как показано ниже.

**Cscript Imp.vbs MNPFren.msi C: \\ Примечание \_ об установщике для \\ французского языка (ошибка).**

Чтобы импортировать и заменить таблицу Актионтекст с помощью Актионте., можно использовать командную строку, как показано ниже.

**Cscript Imp.vbs MNPFren.msi C: \\ Примечание \_ установщик \\ Французская актионте.**

Повторно запустите проверку на MNPFren.msi, как описано в разделе [Проверка обновления установки](validating-an-installation-upgrade.md).

[Продолжить](localizing-database-columns.md)

 

 



