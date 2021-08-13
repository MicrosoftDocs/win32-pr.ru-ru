---
description: Файл преобразования можно создать с помощью Мсидатабасеженератетрансформ или метода GenerateTransform объекта Database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Создание преобразования настройки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636002"
---
# <a name="generating-a-customization-transform"></a>Создание преобразования настройки

Файл преобразования можно создать с помощью [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) или [**метода GenerateTransform**](database-generatetransform.md) [**объекта Database**](database-object.md). пример приведен в установщик Windows SDK в качестве служебной WiGenXfm.vbs. следующий фрагмент кода, Gen.vbs, также иллюстрирует метод **GenerateTransform** и предназначен для использования с Windowsным узлом сценариев.


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

 

 



