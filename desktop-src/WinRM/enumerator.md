---
title: Объект Enumerator (Всмандисп. h)
description: Представляет поток результатов, возвращенных операциями, например операция извлечения.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта перечислителя
- Объект перечислителя служба удаленного управления Windows, описание
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071942"
---
# <a name="enumerator-object"></a>Enumerator - объект

Представляет поток результатов, возвращенных операциями, например операция извлечения. Например, метод [**Session. Enumerate**](session-enumerate.md) возвращает несколько результатов.

## <a name="members"></a>Элементы

Объект **перечислителя** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **перечислителя** содержит эти методы.



| Метод                                  | Описание                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Извлекает элемент из ресурса и возвращает XML-представление элемента.<br/> |



 

### <a name="properties"></a>Свойства

Объект **перечислителя** имеет эти свойства.



| Свойство                                                     | Описание                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**атендофстреам**](enumerator-atendofstream.md)<br/> | Возвращает логическое значение, указывающее, имеется ли в коллекции больше элементов.<br/> |
| [**Ошибка**](enumerator-error.md)<br/>                 | Возвращает XML-представление дополнительных сведений об ошибке.<br/>                         |



 

## <a name="remarks"></a>Комментарии

Чтобы запустить перечисление, используйте [**Session. Enumerate**](session-enumerate.md). Для выполнения операции [*WS-enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) , которая возобновляет чтение элементов в перечислении, используйте [**перечислитель. ReadItem**](enumerator-readitem.md).

Объект **перечислителя** соответствует интерфейсу [**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .

## <a name="examples"></a>Примеры

В следующем примере кода VBScript перечисляются все диски на удаленном компьютере, указанные полным доменным именем (servername.domain.com). Подпрограмма DisplayOutput форматирует выходные данные таким же образом, как средство WinRM. cmd.


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[API сценариев WinRM](winrm-scripting-api.md)
</dt> <dt>

[Перечисление или вывод всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





