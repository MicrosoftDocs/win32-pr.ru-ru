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
# <a name="session-constants"></a><span data-ttu-id="a25dd-103">Константы сеанса</span><span class="sxs-lookup"><span data-stu-id="a25dd-103">Session Constants</span></span>

<span data-ttu-id="a25dd-104">Константы сеанса в перечислении **\_ \_ всмансессионфлагс** указывают проверку подлинности и другие сведения для вызовов [**WSMan. CreateSession**](wsman-createsession.md) или [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) , которые подключаются к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a25dd-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="a25dd-105">Эти константы также тесно связаны с параметрами средства командной строки **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="a25dd-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="a25dd-106">Использование констант сеанса</span><span class="sxs-lookup"><span data-stu-id="a25dd-106">Using Session Constants</span></span>

<span data-ttu-id="a25dd-107">Флаги сеанса для вызова [**WSMan. CreateSession**](wsman-createsession.md) можно задать двумя разными способами.</span><span class="sxs-lookup"><span data-stu-id="a25dd-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="a25dd-108">Один из них короче и проще.</span><span class="sxs-lookup"><span data-stu-id="a25dd-108">One is shorter and simpler.</span></span> <span data-ttu-id="a25dd-109">Более длинный способ, как показано в следующем примере, — это указать значение флага, который вы хотите использовать, и создать в скрипте константу с этим значением.</span><span class="sxs-lookup"><span data-stu-id="a25dd-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="a25dd-110">Затем константа используется для задания значения параметра *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="a25dd-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="a25dd-111">Рекомендуемый способ, как показано в следующем примере, заключается в использовании метода объекта [**WSMan**](wsman.md) , связанного с флагом.</span><span class="sxs-lookup"><span data-stu-id="a25dd-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="a25dd-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Константы проверки подлинности**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a25dd-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a25dd-113">Укажите метод проверки подлинности и способ управления серверами сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a25dd-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="a25dd-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Другие константы сеанса**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a25dd-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a25dd-115">Укажите порт для кодирования, шифрования и имени участника-службы.</span><span class="sxs-lookup"><span data-stu-id="a25dd-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a25dd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a25dd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a25dd-117">Константы и перечисления WinRM</span><span class="sxs-lookup"><span data-stu-id="a25dd-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a25dd-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="a25dd-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="a25dd-119">Проверка подлинности для удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="a25dd-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




