---
title: лаунчпермиссион
description: Описание списка управления доступом (ACL) участников, которые могут запускать новые серверы для этого класса. Это значение можно добавить в любой ключ AppID, чтобы ограничить активацию удаленными клиентами конкретных классов.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- COM-значение реестра Лаунчпермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068625"
---
# <a name="launchpermission"></a>лаунчпермиссион

Описание списка управления доступом (ACL) участников, которые могут запускать новые серверы для этого класса. Это значение можно добавить в любой ключ [**AppID**](appid-key.md) , чтобы ограничить активацию удаленными клиентами конкретных классов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Комментарии

Это **\_ двоичное значение reg** . После получения локального или удаленного запроса на запуск сервера этого класса список ACL, описываемый этим значением, проверяется при олицетворении клиента, и его успешное выполнение либо разрешает, либо запрещает запуск сервера. Если это значение не существует, значение [**дефаултлаунчпермиссион**](defaultlaunchpermission.md) проверяется таким же образом, чтобы определить, можно ли запустить код класса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**дефаултлаунчпермиссион**](defaultlaunchpermission.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 




