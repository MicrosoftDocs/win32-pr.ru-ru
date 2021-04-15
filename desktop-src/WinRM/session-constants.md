---
title: Константы сеанса
description: Константы сеанса в \_ \_ перечислении всмансессионфлагс указывают проверку подлинности и другие сведения для вызовов WSMan. CreateSession или ивсман CreateSession, которые подключаются к удаленному компьютеру.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710033"
---
# <a name="session-constants"></a>Константы сеанса

Константы сеанса в перечислении **\_ \_ всмансессионфлагс** указывают проверку подлинности и другие сведения для вызовов [**WSMan. CreateSession**](wsman-createsession.md) или [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) , которые подключаются к удаленному компьютеру. Эти константы также тесно связаны с параметрами средства командной строки **WinRM** .

## <a name="using-session-constants"></a>Использование констант сеанса

Флаги сеанса для вызова [**WSMan. CreateSession**](wsman-createsession.md) можно задать двумя разными способами. Один из них короче и проще. Более длинный способ, как показано в следующем примере, — это указать значение флага, который вы хотите использовать, и создать в скрипте константу с этим значением. Затем константа используется для задания значения параметра *ифлагс* .

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

Рекомендуемый способ, как показано в следующем примере, заключается в использовании метода объекта [**WSMan**](wsman.md) , связанного с флагом.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Константы проверки подлинности**](authentication-constants.md)
</dt> <dd>

Укажите метод проверки подлинности и способ управления серверами сертификатов.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Другие константы сеанса**](other-session-constants.md)
</dt> <dd>

Укажите порт для кодирования, шифрования и имени участника-службы.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Константы и перечисления WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Проверка подлинности для удаленных подключений](authentication-for-remote-connections.md)
</dt> </dl>

 

 




