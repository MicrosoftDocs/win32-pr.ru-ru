---
title: Конечные точки
description: Настраивает приложение COM для использования указанного номера порта TCP для связи DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Значение реестра для конечных точек COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ee2444be55aaf32c028792100e3e6f0ed6989509b7c0af02c5d83bd739fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048322"
---
# <a name="endpoints"></a>Конечные точки

Настраивает приложение COM для использования указанного номера порта TCP для связи DCOM.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Remarks

Это **\_ \_ SZое значение реестра** .

Значение *Port* — это число от 1024 до 65535, УКАЗЫВАЮЩЕЕ номер TCP-порта, который будет использоваться приложением COM для связи DCOM. Если этот раздел реестра не указан, то номера портов для подключений DCOM назначаются динамически. В большинстве случаев вы можете оставить этот раздел реестра неопределенным и разрешить протоколу DCOM динамически назначать номера портов.

 

 




