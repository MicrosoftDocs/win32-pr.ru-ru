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
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672844"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="74f2e-104">Перечисление Екстендеддисконнектреасонкоде</span><span class="sxs-lookup"><span data-stu-id="74f2e-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="74f2e-105">Определяет расширенные сведения о причине отключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="74f2e-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f2e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74f2e-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="74f2e-107">Константы</span><span class="sxs-lookup"><span data-stu-id="74f2e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="74f2e-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**ексдискреасонноинфо**</span><span class="sxs-lookup"><span data-stu-id="74f2e-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-109">Дополнительные сведения недоступны.</span><span class="sxs-lookup"><span data-stu-id="74f2e-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**ексдискреасонапиинитиатеддисконнект**</span><span class="sxs-lookup"><span data-stu-id="74f2e-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-111">Приложение инициировало отключение.</span><span class="sxs-lookup"><span data-stu-id="74f2e-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**ексдискреасонапиинитиатедлогофф**</span><span class="sxs-lookup"><span data-stu-id="74f2e-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-113">Приложение выполнило выход из системы клиента.</span><span class="sxs-lookup"><span data-stu-id="74f2e-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**ексдискреасонсерверидлетимеаут**</span><span class="sxs-lookup"><span data-stu-id="74f2e-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-115">Сервер отключил клиент, так как он бездействует в течение некоторого времени, чем заданный период времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="74f2e-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**ексдискреасонсерверлогонтимеаут**</span><span class="sxs-lookup"><span data-stu-id="74f2e-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-117">Сервер отключил клиент, так как клиент превысил период, назначенный для подключения.</span><span class="sxs-lookup"><span data-stu-id="74f2e-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**ексдискреасонреплацедбйосерконнектион**</span><span class="sxs-lookup"><span data-stu-id="74f2e-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-119">Подключение клиента было заменено другим соединением.</span><span class="sxs-lookup"><span data-stu-id="74f2e-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**ексдискреасонаутофмемори**</span><span class="sxs-lookup"><span data-stu-id="74f2e-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-121">Нет доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="74f2e-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**ексдискреасонсервердениедконнектион**</span><span class="sxs-lookup"><span data-stu-id="74f2e-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-123">Сервер отклонил подключение.</span><span class="sxs-lookup"><span data-stu-id="74f2e-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**ексдискреасонсервердениедконнектионфипс**</span><span class="sxs-lookup"><span data-stu-id="74f2e-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-125">Сервер отклонил подключение по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="74f2e-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**ексдискреасонсерверинсуффиЦиентпривилежес**</span><span class="sxs-lookup"><span data-stu-id="74f2e-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-127">Сервер отклонил подключение по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="74f2e-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**ексдискреасонсерверфрешкредсрекуиред**</span><span class="sxs-lookup"><span data-stu-id="74f2e-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-129">Требуются новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="74f2e-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**ексдискреасонрпЦинитиатеддисконнектбюсер**</span><span class="sxs-lookup"><span data-stu-id="74f2e-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-131">Действие пользователя инициировало отключение.</span><span class="sxs-lookup"><span data-stu-id="74f2e-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**ексдискреасонлогоффбюсер**</span><span class="sxs-lookup"><span data-stu-id="74f2e-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-133">Пользователь вышел из системы, отключающий сеанс.</span><span class="sxs-lookup"><span data-stu-id="74f2e-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**ексдискреасонлиценсеинтернал**</span><span class="sxs-lookup"><span data-stu-id="74f2e-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-135">Внутренняя ошибка лицензирования.</span><span class="sxs-lookup"><span data-stu-id="74f2e-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**ексдискреасонлиценсенолиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="74f2e-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-137">Сервер лицензирования недоступен.</span><span class="sxs-lookup"><span data-stu-id="74f2e-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**ексдискреасонлиценсенолиценсе**</span><span class="sxs-lookup"><span data-stu-id="74f2e-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-139">Действительная лицензия на программное обеспечение недоступна.</span><span class="sxs-lookup"><span data-stu-id="74f2e-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**ексдискреасонлиценсиррклиентмсг**</span><span class="sxs-lookup"><span data-stu-id="74f2e-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-141">Удаленный компьютер получил недействительное сообщение лицензирования.</span><span class="sxs-lookup"><span data-stu-id="74f2e-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**ексдискреасонлиценсехвиддоеснтматчлиценсе**</span><span class="sxs-lookup"><span data-stu-id="74f2e-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-143">Идентификатор оборудования не соответствует указанному в лицензии на программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="74f2e-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**ексдискреасонлиценсиррклиентлиценсе**</span><span class="sxs-lookup"><span data-stu-id="74f2e-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-145">Ошибка клиентской лицензии.</span><span class="sxs-lookup"><span data-stu-id="74f2e-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**ексдискреасонлиценсекантфинишпротокол**</span><span class="sxs-lookup"><span data-stu-id="74f2e-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-147">Во время протокола лицензирования возникли проблемы с сетью.</span><span class="sxs-lookup"><span data-stu-id="74f2e-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**ексдискреасонлиценсеклиентендедпротокол**</span><span class="sxs-lookup"><span data-stu-id="74f2e-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-149">Клиент преждевременно завершил работу протокола лицензирования.</span><span class="sxs-lookup"><span data-stu-id="74f2e-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**ексдискреасонлиценсиррклиентенкриптион**</span><span class="sxs-lookup"><span data-stu-id="74f2e-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-151">Сообщение лицензирования было зашифровано неправильно.</span><span class="sxs-lookup"><span data-stu-id="74f2e-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**ексдискреасонлиценсекантупграделиценсе**</span><span class="sxs-lookup"><span data-stu-id="74f2e-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-153">Не удалось обновить или обновить клиентскую лицензию на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="74f2e-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**ексдискреасонлиценсеноремотеконнектионс**</span><span class="sxs-lookup"><span data-stu-id="74f2e-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-155">Удаленный компьютер не имеет лицензии на прием удаленных подключений.</span><span class="sxs-lookup"><span data-stu-id="74f2e-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**ексдискреасонлиценсекреатингликстореаккдениед**</span><span class="sxs-lookup"><span data-stu-id="74f2e-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-157">При создании раздела реестра для хранилища лицензий была получена ошибка "отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="74f2e-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**ексдискреасонрдпенЦинвалидкредентиалс**</span><span class="sxs-lookup"><span data-stu-id="74f2e-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-159">Обнаружены недопустимые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="74f2e-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**ексдискреасонпротоколранжестарт**</span><span class="sxs-lookup"><span data-stu-id="74f2e-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-161">Начало диапазона внутренних ошибок протокола.</span><span class="sxs-lookup"><span data-stu-id="74f2e-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="74f2e-162">Дополнительные сведения см. в журнале событий сервера.</span><span class="sxs-lookup"><span data-stu-id="74f2e-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="74f2e-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**ексдискреасонпротоколранжеенд**</span><span class="sxs-lookup"><span data-stu-id="74f2e-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="74f2e-164">Завершение диапазона внутренних ошибок протокола.</span><span class="sxs-lookup"><span data-stu-id="74f2e-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74f2e-165">Требования</span><span class="sxs-lookup"><span data-stu-id="74f2e-165">Requirements</span></span>



| <span data-ttu-id="74f2e-166">Требование</span><span class="sxs-lookup"><span data-stu-id="74f2e-166">Requirement</span></span> | <span data-ttu-id="74f2e-167">Значение</span><span class="sxs-lookup"><span data-stu-id="74f2e-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74f2e-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74f2e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="74f2e-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74f2e-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="74f2e-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74f2e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="74f2e-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74f2e-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="74f2e-172">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="74f2e-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="74f2e-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74f2e-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f2e-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74f2e-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f2e-175">**екстендеддисконнектреасон**</span><span class="sxs-lookup"><span data-stu-id="74f2e-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





