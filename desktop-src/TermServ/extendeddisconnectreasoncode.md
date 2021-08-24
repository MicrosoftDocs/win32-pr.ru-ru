---
title: Перечисление Екстендеддисконнектреасонкоде
description: Определяет расширенные сведения о причине отключения элемента управления.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Екстендеддисконнектреасонкоде
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cfb917e2a74b82b55dc91a507e2c5815fbe83c632c4b3e29eb76941ab07662e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737844"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a>Перечисление Екстендеддисконнектреасонкоде

Определяет расширенные сведения о причине отключения элемента управления.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**ексдискреасонноинфо**
</dt> <dd>

Дополнительные сведения недоступны.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**ексдискреасонапиинитиатеддисконнект**
</dt> <dd>

Приложение инициировало отключение.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**ексдискреасонапиинитиатедлогофф**
</dt> <dd>

Приложение выполнило выход из системы клиента.

</dd> <dt>

<span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**ексдискреасонсерверидлетимеаут**
</dt> <dd>

Сервер отключил клиент, так как он бездействует в течение некоторого времени, чем заданный период времени ожидания.

</dd> <dt>

<span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**ексдискреасонсерверлогонтимеаут**
</dt> <dd>

Сервер отключил клиент, так как клиент превысил период, назначенный для подключения.

</dd> <dt>

<span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**ексдискреасонреплацедбйосерконнектион**
</dt> <dd>

Подключение клиента было заменено другим соединением.

</dd> <dt>

<span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**ексдискреасонаутофмемори**
</dt> <dd>

Нет доступной памяти.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**ексдискреасонсервердениедконнектион**
</dt> <dd>

Сервер отклонил подключение.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**ексдискреасонсервердениедконнектионфипс**
</dt> <dd>

Сервер отклонил подключение по соображениям безопасности.

</dd> <dt>

<span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**ексдискреасонсерверинсуффиЦиентпривилежес**
</dt> <dd>

Сервер отклонил подключение по соображениям безопасности.

</dd> <dt>

<span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**ексдискреасонсерверфрешкредсрекуиред**
</dt> <dd>

Требуются новые учетные данные.

</dd> <dt>

<span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**ексдискреасонрпЦинитиатеддисконнектбюсер**
</dt> <dd>

Действие пользователя инициировало отключение.

</dd> <dt>

<span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**ексдискреасонлогоффбюсер**
</dt> <dd>

Пользователь вышел из системы, отключающий сеанс.

</dd> <dt>

<span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**ексдискреасонлиценсеинтернал**
</dt> <dd>

Внутренняя ошибка лицензирования.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**ексдискреасонлиценсенолиценсесервер**
</dt> <dd>

Сервер лицензирования недоступен.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**ексдискреасонлиценсенолиценсе**
</dt> <dd>

Действительная лицензия на программное обеспечение недоступна.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**ексдискреасонлиценсиррклиентмсг**
</dt> <dd>

Удаленный компьютер получил недействительное сообщение лицензирования.

</dd> <dt>

<span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**ексдискреасонлиценсехвиддоеснтматчлиценсе**
</dt> <dd>

Идентификатор оборудования не соответствует указанному в лицензии на программное обеспечение.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**ексдискреасонлиценсиррклиентлиценсе**
</dt> <dd>

Ошибка клиентской лицензии.

</dd> <dt>

<span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**ексдискреасонлиценсекантфинишпротокол**
</dt> <dd>

Во время протокола лицензирования возникли проблемы с сетью.

</dd> <dt>

<span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**ексдискреасонлиценсеклиентендедпротокол**
</dt> <dd>

Клиент преждевременно завершил работу протокола лицензирования.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**ексдискреасонлиценсиррклиентенкриптион**
</dt> <dd>

Сообщение лицензирования было зашифровано неправильно.

</dd> <dt>

<span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**ексдискреасонлиценсекантупграделиценсе**
</dt> <dd>

Не удалось обновить или обновить клиентскую лицензию на локальном компьютере.

</dd> <dt>

<span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**ексдискреасонлиценсеноремотеконнектионс**
</dt> <dd>

Удаленный компьютер не имеет лицензии на прием удаленных подключений.

</dd> <dt>

<span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**ексдискреасонлиценсекреатингликстореаккдениед**
</dt> <dd>

При создании раздела реестра для хранилища лицензий была получена ошибка "отказано в доступе".

</dd> <dt>

<span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**ексдискреасонрдпенЦинвалидкредентиалс**
</dt> <dd>

Обнаружены недопустимые учетные данные.

</dd> <dt>

<span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**ексдискреасонпротоколранжестарт**
</dt> <dd>

Начало диапазона внутренних ошибок протокола. Дополнительные сведения см. в журнале событий сервера.

</dd> <dt>

<span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**ексдискреасонпротоколранжеенд**
</dt> <dd>

Завершение диапазона внутренних ошибок протокола.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**екстендеддисконнектреасон**](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





