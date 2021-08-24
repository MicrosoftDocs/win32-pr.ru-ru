---
title: сервицепараметерс
description: Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM-значение реестра Сервицепараметерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129966"
---
# <a name="serviceparameters"></a>сервицепараметерс

Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** . Эта строка передается в службу в виде аргумента командной строки при запуске.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**локальная служба.**](localservice.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> </dl>

 

 




