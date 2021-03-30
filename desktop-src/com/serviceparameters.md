---
title: сервицепараметерс
description: Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM-значение реестра Сервицепараметерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330163"
---
# <a name="serviceparameters"></a>сервицепараметерс

Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** . Эта строка передается в службу в виде аргумента командной строки при запуске.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**локальная служба.**](localservice.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> </dl>

 

 




