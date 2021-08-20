---
title: Метод Жетложевентнаме класса Win32_TSGatewayServerSettings
description: Возвращает имя события журнала для указанного индекса событий журнала.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетложевентнаме
- Службы удаленных рабочих столов метода Жетложевентнаме, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетложевентнаме
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da065826045de51b94a1f4c5dec58a78f52d761d6b694017332d9d6558cb273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130621"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Жетложевентнаме \_ класса Win32 тсгатевайсерверсеттингс

Возвращает имя события журнала для указанного индекса событий журнала.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Евентиндекс* \[ окне\]
</dt> <dd>

Индекс события журнала. Значение должно быть в диапазоне от нуля до значения свойства **максложевентс** .

</dd> <dt>

*EventName* \[ заполняет\]
</dt> <dd>

Имя указанного события. В следующем списке приведены возможные значения.

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**логчаннелдисконнект**


</dt> <dd>

Пользователь успешно отключился от ресурса.

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**логфаилуречаннелконнект**


</dt> <dd>

Пользователю не удалось подключиться к ресурсу.

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**логфаилуреконнектионаусоризатиончекк**


</dt> <dd>

Пользователь не прошел авторизацию подключения.

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**логфаилурересаурцеаусоризатиончекк**


</dt> <dd>

Пользователь не прошел авторизацию ресурсов.

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**логсукцессфулчаннелконнект**


</dt> <dd>

Пользователь успешно подключился к ресурсу.

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**логсукцессфулконнектионаусоризатиончекк**


</dt> <dd>

Пользователь успешно прошел авторизацию подключения.

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**логсукцессфулресаурцеаусоризатиончекк**


</dt> <dd>

Пользователь успешно прошел авторизацию ресурсов.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**енаблеложевент**](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[**исложевентенаблед**](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

