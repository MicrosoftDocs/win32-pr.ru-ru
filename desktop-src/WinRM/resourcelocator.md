---
title: Объект ResourceLocator (Всмандисп. h)
description: Предоставляет путь к ресурсу. Вы можете использовать объект ResourceLocator вместо URI ресурса в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, описание
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135311"
---
# <a name="resourcelocator-object"></a>Объект ResourceLocator

Объект, предоставляющий путь к ресурсу. Вы можете использовать объект **ResourceLocator** вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

Этот объект позволяет выполнять следующие задачи:

-   Добавьте один или несколько [*селекторов*](windows-remote-management-glossary.md) , которые указывают конкретный экземпляр ресурса. Это то же самое, что и указание значения ключа в универсальном коде ресурса (URI) ресурса, использующего ключи. Дополнительные сведения см. в разделе [**ResourceLocator. аддселектор**](resourcelocator-addselector.md). Аналогичную операцию можно выполнить с помощью параметра *Filter* в вызове [**Session. Enumerate**](session-enumerate.md).
-   Укажите путь [*фрагмента*](windows-remote-management-glossary.md) и диалект, чтобы получить только одно свойство ресурса. Можно также указать один или все элементы свойства массива, указав индекс массива. Дополнительные сведения см. в разделе [**ResourceLocator. фрагментпас**](resourcelocator-fragmentpath.md).
-   Добавьте один или несколько [*параметров*](windows-remote-management-glossary.md) , которые могут потребоваться источнику данных для обработки запроса. Дополнительные сведения см. в разделе [**ResourceLocator. аддоптион**](resourcelocator-addoption.md).

Дополнительные сведения см. в разделе [запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Элементы

Объект **ResourceLocator** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **ResourceLocator** содержит эти методы.



| Метод                                                   | Описание                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**аддоптион**](resourcelocator-addoption.md)           | Добавляет дополнительные данные, необходимые для обработки запроса.<br/>                                                                   |
| [**аддселектор**](resourcelocator-addselector.md)       | Добавляет [*селектор*](windows-remote-management-glossary.md) в объект **ResourceLocator** .<br/>     |
| [**клеароптионс**](resourcelocator-clearoptions.md)     | Удаляет все [*Параметры*](windows-remote-management-glossary.md) из объекта **ResourceLocator** .<br/> |
| [**клеарселекторс**](resourcelocator-clearselectors.md) | Удаляет все селекторы из объекта **ResourceLocator** .<br/>                                                            |



 

### <a name="properties"></a>Свойства

Объект **ResourceLocator** имеет следующие свойства.



| Свойство                                                                          | Тип доступа           | Описание                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**фрагментдиалект**](resourcelocator-fragmentdialect.md)<br/>             | Чтение/запись<br/> | Возвращает или задает диалект языка для [*фрагмента*](windows-remote-management-glossary.md) [*ресурса*](windows-remote-management-glossary.md) .<br/> |
| [**фрагментпас**](resourcelocator-fragmentpath.md)<br/>                   | Чтение/запись<br/> | Возвращает или задает путь к [*фрагменту*](windows-remote-management-glossary.md) или свойству [*ресурса*](windows-remote-management-glossary.md) .<br/> |
| [**мустундерстандоптионс**](resourcelocator-mustunderstandoptions.md)<br/> | Чтение/запись<br/> | Возвращает или задает значение **мустундерстандоптионс** для объекта **ResourceLocator** .<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Чтение/запись<br/> | Возвращает или задает [*URI ресурса*](windows-remote-management-glossary.md) в объекте **ResourceLocator** .<br/>                                                          |



 

## <a name="remarks"></a>Комментарии

Объект **ResourceLocator** соответствует интерфейсу **ивсманресаурцелокатор** .

## <a name="examples"></a>Примеры

Следующий пример кода VBScript получает свойства **нумберофлогикалпроцессорс** и **нумберофкорес** из определенного экземпляра [**\_ процессора Win32**](/windows/desktop/CIMWin32Prov/win32-processor).


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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
</dt> </dl>

 

