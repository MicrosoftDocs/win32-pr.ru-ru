---
title: Метод Enumerator. ReadItem (Всмандисп. h)
description: Извлекает элемент из ресурса и возвращает XML-представление элемента.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода ReadItem
- служба удаленного управления Windows метода ReadItem, объект Enumerator
- объект перечислителя служба удаленного управления Windows, метод ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a24109d22c4fc114513c2113af48c62a7042cd90feb075718e57323ecf5238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993814"
---
# <a name="enumeratorreaditem-method"></a>Метод Enumerator. ReadItem

Извлекает элемент из ресурса и возвращает XML-представление элемента.

## <a name="syntax"></a>Синтаксис


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*resource* 
</dt> <dd>

URI элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

XML-представление элемента.

## <a name="remarks"></a>Remarks

Чтобы ограничить количество считываемых элементов, задайте свойство [**Session.Batчитемс**](session-batchitems.md) .

Обратите внимание, что освобождение объекта перечисления очищает все ожидающие запросы перечисления.

Метод [**Session. Enumerate**](session-enumerate.md) не получает коллекцию точно так же, как [запрос WMI](/windows/desktop/WmiSdk/querying-wmi), такой как `SELECT * from Win32_LogicalDisk` , возвращает коллекцию в [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset). Для чтения файла в виде текстового потока создается объект скрипта [TextStream](/previous-versions//312a5kbt(v=vs.85)) и вызывается метод [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) для чтения каждой строки файла. Аналогичным образом вызывается метод **Session. Enumerate** для получения объекта [**перечислителя**](enumerator.md) , а затем вызывается метод **Enumerator. ReadItem** . Как и при чтении из текстового файла, можно проверить свойство [**Enumerator. атендофстреам**](enumerator-atendofstream.md) , чтобы проверить, достигли ли вы конца элементов данных.

## <a name="examples"></a>Примеры

В следующем примере VBScript вызывается метод [**Session. Enumerate**](session-enumerate.md) для получения списка запланированных заданий. Подпрограмма DisplayOutput использует XML-файл преобразования средства командной строки WinRM (Всмткст. xsl) для вывода данных в табличной форме.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Перечислитель**](enumerator.md)
</dt> <dt>

[Перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

