---
title: Конечные точки
description: Настраивает приложение COM для использования указанного номера порта TCP для связи DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Значение реестра для конечных точек COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410793"
---
# <a name="endpoints"></a><span data-ttu-id="9cec9-104">Конечные точки</span><span class="sxs-lookup"><span data-stu-id="9cec9-104">Endpoints</span></span>

<span data-ttu-id="9cec9-105">Настраивает приложение COM для использования указанного номера порта TCP для связи DCOM.</span><span class="sxs-lookup"><span data-stu-id="9cec9-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9cec9-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="9cec9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="9cec9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cec9-107">Remarks</span></span>

<span data-ttu-id="9cec9-108">Это **\_ \_ SZое значение реестра** .</span><span class="sxs-lookup"><span data-stu-id="9cec9-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="9cec9-109">Значение *Port* — это число от 1024 до 65535, УКАЗЫВАЮЩЕЕ номер TCP-порта, который будет использоваться приложением COM для связи DCOM.</span><span class="sxs-lookup"><span data-stu-id="9cec9-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="9cec9-110">Если этот раздел реестра не указан, то номера портов для подключений DCOM назначаются динамически.</span><span class="sxs-lookup"><span data-stu-id="9cec9-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="9cec9-111">В большинстве случаев вы можете оставить этот раздел реестра неопределенным и разрешить протоколу DCOM динамически назначать номера портов.</span><span class="sxs-lookup"><span data-stu-id="9cec9-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




