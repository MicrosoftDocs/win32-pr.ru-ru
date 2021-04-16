---
description: Файл преобразования можно создать с помощью Мсидатабасеженератетрансформ или метода GenerateTransform объекта Database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Создание преобразования настройки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650944"
---
# <a name="generating-a-customization-transform"></a>Создание преобразования настройки

Файл преобразования можно создать с помощью [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) или [**метода GenerateTransform**](database-generatetransform.md) [**объекта Database**](database-object.md). Пример приведен в установщик Windows SDK в качестве служебной WiGenXfm.vbs. Следующий фрагмент кода, Gen.vbs, также иллюстрирует метод **GenerateTransform** и предназначен для использования с сервером сценариев Windows.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Чтобы создать файл преобразования Мнптранс. MST из исходной базы данных MNP2000.msi и MNP2000t.msi базы данных, измененной при [настройке исходной базы данных](customizing-an-original-database.md), измените каталоги на папку, содержащую Gen.vbs, исходную базу данных и обновленную базу данных установщика, а затем введите следующую командную строку.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi Мнптранс. MST**

[Продолжить](adding-summary-information-to-customization-transform.md)

 

 



