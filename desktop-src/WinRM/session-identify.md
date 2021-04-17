---
title: Метод Session. Identify (Всмандисп. h)
description: Запрашивает удаленный компьютер, чтобы определить, поддерживает ли он протокол WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Выявление служба удаленного управления Windows метода
- Обнаружение служба удаленного управления Windows метода, объект Session
- Объект Session служба удаленного управления Windows, метод Identify
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710535"
---
# <a name="sessionidentify-method"></a>Метод Session. Identify

Метод **Session. Identify** запрашивает удаленный компьютер, чтобы определить, поддерживает ли он протокол WS-Management. Дополнительные сведения см. [в разделе Определение того, поддерживает ли удаленный компьютер протокол WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Синтаксис


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Чтобы отправить запрос в режиме с проверкой подлинности, используйте константу проверки подлинности из перечисления **всмансессионфлагс** . Для отправки в режиме без проверки подлинности используйте **всманфлагусеноаусентикатион**. Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

XML-строка, указывающая версию протокола WS-Management, поставщика операционной системы и, если запрос был отправлен с проверкой подлинности, версия операционной системы.

## <a name="remarks"></a>Комментарии

**Сеанс. Identify** основан на операции [протокол WS-Management](ws-management-protocol.md) , определенной как всманидентити. Это указывается в пакете SOAP следующим образом:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Примеры

Следующий пример на языке VBScript отправляет на удаленный компьютер с именем Remote запрос на выявление запроса на проверку без проверки подлинности в том же домене.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
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

[**Session**](session.md)
</dt> <dt>

[**IWSManSession:: Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Протокол WS-Management](ws-management-protocol.md)
</dt> </dl>

 

 





