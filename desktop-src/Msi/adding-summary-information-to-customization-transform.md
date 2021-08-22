---
description: Чтобы применить преобразование настройки во время установки продукта, необходимо добавить информационный поток сводки в файл преобразования Мнптранс. MST, созданный при формировании преобразования настройки.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Добавление сводных данных в преобразование настройки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ea4c9aa505d425bfd06fe5cac1f45666e794624618db14100ee5f517dd3048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639474"
---
# <a name="adding-summary-information-to-customization-transform"></a>Добавление сводных данных в преобразование настройки

Чтобы применить преобразование настройки во время установки продукта, необходимо добавить [информационный поток сводки](summary-information-stream.md) в файл преобразования мнптранс. MST, созданный при [формировании преобразования настройки](generating-a-customization-transform.md).

Вы можете создать сводные данные для преобразования с помощью [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) или [**метода креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md). следующий фрагмент кода, Sum.vbs, иллюстрирует [**метод креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md) и предназначен для использования с Windowsным узлом сценариев. Обратите внимание, что этот пример не выполняет проверку и подавляет состояние ошибки.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Чтобы создать и добавить сводные данные в файл преобразования Мнптранс. MST, созданный при [формировании преобразования настройки](generating-a-customization-transform.md), измените каталоги на папку, содержащую Gen.vbs, исходную базу данных, обновленную базу данных и преобразование, а затем введите следующую командную строку.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi Мнптранс. MST**

Щелкните значок MNP2000.msi, чтобы запустить установку, или используйте следующую командную строку.

**msiexec/i MNP2000.msi**

При этом продукт устанавливается без настроек. Чтобы установить с настройками, введите следующую командную строку. Обратите внимание, что значение [**Свойства**](transforms.md) Transforms ссылается на файл преобразования, расположенный в источнике.

**msiexec/i MNP2000.msi преобразования = Мнптранс. MST**

Функция шлюза не отображается в дереве выбора компонентов, а компоненты компонента шлюза не устанавливаются, даже если в пользовательском интерфейсе выбран полный тип установки.

[Продолжить](embedding-customization-transforms-as-substorage.md)

 

 



