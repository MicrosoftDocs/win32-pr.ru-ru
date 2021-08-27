---
title: Метод Session. Create (Всмандисп. h)
description: Создает новый экземпляр ресурса и возвращает ссылку на конечную точку (EPR) нового объекта.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Create
- создание служба удаленного управления Windows метода, объект Session
- объект Session служба удаленного управления Windows, метод Create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823266"
---
# <a name="sessioncreate-method"></a>Метод Session. Create

Создает новый экземпляр ресурса и возвращает [*ссылку на конечную точку (EPR)*](windows-remote-management-glossary.md) нового объекта.

## <a name="syntax"></a>Синтаксис


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*resourceUri* \[ окне\]
</dt> <dd>

Идентификатор создаваемого ресурса.

Этот параметр может содержать одно из следующих:

-   Универсальный код ресурса (URI) с одним или несколькими [*селекторами*](windows-remote-management-glossary.md). Имейте в виду, что [*подключаемый модуль WMI*](windows-remote-management-glossary.md) не поддерживает создание ресурсов, отличных от прослушивателя [протокол WS-Management](ws-management-protocol.md) .
-   Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).
-   Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management. Дополнительные сведения о общедоступной спецификации для протокола WS-Management см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*resource* 
</dt> <dd>

XML-код, содержащий содержимое ресурса.

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

EPR нового ресурса.

## <a name="remarks"></a>Remarks

**Сеанс. Create** используется только для создания новых экземпляров ресурса. Используйте метод [**Session. помещаем**](session-put.md) для обновления существующих экземпляров ресурса. После получения нового универсального кода ресурса (URI) можно вызвать [**сеанс. Get**](session-get.md) , чтобы получить новый объект. Новый объект содержит все свойства, назначаемые поставщиком ресурсов при создании нового объекта. Например, если создать новый [*прослушиватель*](windows-remote-management-glossary.md) протокола WS-Management и получить объект прослушивателя с помощью **сеанса. Get**, то вы получаете также свойства **Port**, **Enabled** и **листенингон** .

Имейте в виду, что [*подключаемый модуль WMI*](windows-remote-management-glossary.md) не поддерживает создание каких-либо ресурсов, кроме прослушивателя протокола WS-Management.

Для вызова этого метода используется следующий синтаксис.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Примеры

В следующем примере кода на языке VBScript вызывается **сеанс. Create** для создания прослушивателя на локальном компьютере.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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

[**Сеанс**](session.md)
</dt> <dt>

[Протокол WS-Management](ws-management-protocol.md)
</dt> </dl>

 

