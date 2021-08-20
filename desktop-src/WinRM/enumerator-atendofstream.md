---
title: Свойство Enumerator. Атендофстреам (Всмандисп. h)
description: Возвращает логическое значение, указывающее, имеются ли в коллекции другие элементы.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства атендофстреам
- служба удаленного управления Windows свойства атендофстреам, объект Enumerator
- служба удаленного управления Windows объекта перечислителя, свойство атендофстреам
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1077837f82d650b57dfea0316ef15094b18749eefdb6957e62e6afd92cfe672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113205"
---
# <a name="enumeratoratendofstream-property"></a>Свойство Enumerator. Атендофстреам

Возвращает логическое значение, указывающее, имеются ли в коллекции другие элементы.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Значение свойства

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**Условия**


</dt> <dd>

В коллекции больше нет элементов.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**IsFalse**


</dt> <dd>

Доступны дополнительные элементы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если объект [**перечислителя**](enumerator.md) освобождается после получения всех необходимых данных, все ожидающие запросы перечисления удаляются. Дополнительные сведения см. [в разделе перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="examples"></a>Примеры

В следующем примере на языке VBScript перечисляются экземпляры операционной системы. Обратите внимание, что освобождение объекта перечисления очищает все ожидающие запросы перечисления. Подпрограмма DisplayOutput форматирует выходные данные таким же образом, как средство WinRM. cmd.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Перечислитель**](enumerator.md)
</dt> <dt>

[Перечисление или вывод всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





