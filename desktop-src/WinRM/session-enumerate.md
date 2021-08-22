---
title: Метод Session. reenumerate (Всмандисп. h)
description: Перечисляет таблицу, коллекцию данных или ресурс журнала.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода перечисления
- служба удаленного управления Windows метода перечисления, объект Session
- объект Session служба удаленного управления Windows, enumerate, метод
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642634"
---
# <a name="sessionenumerate-method"></a>Session. Enumerate, метод

Перечисляет таблицу, коллекцию данных или ресурс журнала. Чтобы создать запрос, включите параметр *фильтра* и параметр- *диалект* в перечисление. Для создания запросов также можно использовать объект [**ResourceLocator**](resourcelocator.md) . Дополнительные сведения см. [в разделе перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="syntax"></a>Синтаксис


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*resourceUri* \[ окне\]
</dt> <dd>

Идентификатор извлекаемого ресурса.

Этот параметр может содержать одно из следующих:

-   Универсальный код ресурса (URI) для данного ресурса.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Объект [**ResourceLocator**](resourcelocator.md) .
-   Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management. Дополнительные сведения о общедоступной спецификации для [протокол WS-Management](ws-management-protocol.md)см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Фильтр* \[ в необязательное\]
</dt> <dd>

Фильтр, который определяет, какие элементы в ресурсе возвращаются перечислением. При перечислении ресурса возвращаются только те элементы, которые соответствуют условиям фильтра. Включение параметра *фильтра* и параметра *диалекта* в перечисление преобразует перечисление в запрос. Пример см. в разделе [запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md).

Если у вас есть объект [**ResourceLocator**](resourcelocator.md) для параметра *resourceURI* , этот параметр использовать не следует.

</dd> <dt>

*диалект* \[ в необязательное\]
</dt> <dd>

Язык, используемый фильтром. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi)— подмножество SQL, используемое WMI, является единственным поддерживаемым языком.

Если у вас есть объект [**ResourceLocator**](resourcelocator.md) для параметра *resourceURI* , этот параметр использовать не следует.

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Параметр, который должен содержать флаг в перечислении **\_ \_ всманенумфлагс** . Дополнительные сведения см. в разделе [константы перечисления](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**перечислителя**](enumerator.md) , содержащий результаты перечисления.

## <a name="remarks"></a>Remarks

Дополнительные сведения об ограничении сетевых вызовов во время перечисления см. в описании свойства [**батчитемс**](session-batchitems.md) .

имейте в виду, что если флаги содержат [**константы перечисления**](enumeration-constants.md) **всманфлагхиерарчидипбасепропсонли** или **всманфлагхиерарчишаллов** , то служба удаленного управления Windows служба возвращает код ошибки, **\_ \_ \_ \_ не поддерживаемый режимом полиморфизма WSMAN**.

Если задан фильтр, он должен быть допустимым документом в отношении схемы ресурса. Параметр диалекта является необязательным. Однако если строка фильтра начинается с <, но не является фрагментом XML, следует либо включить параметр *диалекта* , либо установить флаг **всманфлагнонксмлтекст** в параметре *flags* . Дополнительные сведения см. в разделе [**константы перечисления**](enumeration-constants.md).

Соответствующий метод C++ — [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Примеры

Следующий пример кода VBScript перечисляет экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) на удаленном компьютере, указанном в полном доменном имени (servername.domain.com). Имейте в виду, что освобождение объектов перечисления, ожидающих запросов перечисления. Подпрограмма DisplayOutput использует XML-файл преобразования средства командной строки WinRM (Всмткст. xsl) для вывода данных в табличной форме.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

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

[**Сеанс**](session.md)
</dt> <dt>

[Запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**батчитемс**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

