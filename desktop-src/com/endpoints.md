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
# <a name="endpoints"></a>Конечные точки

Настраивает приложение COM для использования указанного номера порта TCP для связи DCOM.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Комментарии

Это **\_ \_ SZое значение реестра** .

Значение *Port* — это число от 1024 до 65535, УКАЗЫВАЮЩЕЕ номер TCP-порта, который будет использоваться приложением COM для связи DCOM. Если этот раздел реестра не указан, то номера портов для подключений DCOM назначаются динамически. В большинстве случаев вы можете оставить этот раздел реестра неопределенным и разрешить протоколу DCOM динамически назначать номера портов.

 

 




