---
description: Метод Ластерроррекорд объекта Installer возвращает объект Record, содержащий параметры ошибки для самой последней ошибки из функции, которая вызвала запись об ошибке.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Метод Installer. Ластерроррекорд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142113"
---
# <a name="installerlasterrorrecord-method"></a>Метод Installer. Ластерроррекорд

Метод **ластерроррекорд** объекта [**Installer**](installer-object.md) возвращает объект [**Record**](record-object.md) , содержащий параметры ошибки для самой последней ошибки из функции, которая вызвала запись об ошибке.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Объект [**Record**](record-object.md) сбрасывается после выполнения этой функции любой функции, которая создает запись об ошибке.

Только следующие назначенные функции создают запись об ошибке:

-   [**Метод Опендатабасе (объект установщика)**](installer-opendatabase.md)
-   [**Фиксация**](database-commit.md)
-   [**OpenView**](database-openview.md)
-   [**Импорт**](database-import.md)
-   [**Экспорт**](database-export.md)
-   [**AutoMerge**](database-merge.md)
-   [**Преобразование**](database-generatetransform.md)
-   [**апплитрансформ**](database-applytransform.md)
-   [**Работать**](view-execute.md)
-   [**Изменить**](view-modify.md)
-   [**сетстреам**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**компоненткуррентстате**](session-componentcurrentstate.md)
-   [**компонентрекуестстате**](session-componentrequeststate.md)
-   [**феатурекуррентстате**](session-featurecurrentstate.md)
-   [**феатуререкуестстате**](session-featurerequeststate.md)
-   [**феатурекост**](session-featurecost.md)
-   [**феатуревалидстатес**](session-featurevalidstates.md)
-   [**сетинсталллевел**](session-setinstalllevel.md)

Следующий пример в языке VBScript использует вызов [**опендатабасе**](installer-opendatabase.md) , чтобы продемонстрировать, как получить расширенные сведения об ошибке из одного из методов или свойств, поддерживающих метод **ластерроррекорд** . В примере создается сообщение об ошибке при сбое метода **опендатабасе** . Объект **Err** используется для определения того, была ли обнаружена ошибка.


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




