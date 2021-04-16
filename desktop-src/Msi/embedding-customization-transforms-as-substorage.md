---
description: Преобразование настройки можно сохранить в хранилище пакета установщик Windows, чтобы гарантировать, что преобразование всегда будет доступно при доступности пакета установки.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Внедрение преобразований настройки в качестве подхранилища
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650863"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Внедрение преобразований настройки в качестве подхранилища

Преобразование настройки можно сохранить в хранилище пакета установщик Windows, чтобы гарантировать, что преобразование всегда будет доступно при доступности пакета установки. См. статью [встроенные преобразования](embedded-transforms.md). Пример приведен в установщик Windows SDK в качестве служебной WiSubStg.vbs. В следующем фрагменте кода, Emb.vbs, также показано использование [таблицы хранилищ](-storages-table.md) для добавления внедренного преобразования и предназначено для использования с сервером сценариев Windows.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Чтобы добавить хранилище с именем MNPtrans1 в MNP2000.msi и содержащее преобразование, созданное при [добавлении сводных данных к преобразованию настройки](adding-summary-information-to-customization-transform.md), измените каталоги на папку, содержащую Emb.vbs, исходную базу данных и файл преобразования, а затем введите следующую командную строку.

**Cscript.exe Emb.vbs MNP2000.msi Мнптранс. MST MNPtrans1**

Это завершает пример преобразования настройки. После внедрения преобразования в Мнптранс. MST преобразование всегда доступно в пакете установки. Файл Мнптранс. MST не должен располагаться в источнике, чтобы применить преобразование.

Удалите Мнптранс. MST из папки, содержащей образец установочного пакета. Щелкните значок MNP2000.msi, чтобы запустить установку, или используйте следующую командную строку.

**msiexec/i MNP2000.msi**

Обратите внимание, что при этом устанавливается продукт без настроек. Чтобы установить с настройками, введите следующую команду в командной строке. Используйте двоеточие, чтобы указать, что [**значение свойства**](transforms.md) Transforms ссылается на встроенное преобразование.

msiexec/i MNP2000.msi преобразования =: MNPtrans1

Обратите внимание, что функция шлюза не отображается в дереве выбора компонентов и компоненты компонента шлюза не установлены, даже если в пользовательском интерфейсе выбран полный тип установки.

## <a name="next-example"></a>Следующий пример

[Пример небольшого обновления исправлений](a-small-update-patching-example.md)

 

 



