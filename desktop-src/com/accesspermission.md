---
title: акцесспермиссион
description: Описывает список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса. Этот список ACL используется только приложениями, которые не вызывают CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- COM-значение реестра Акцесспермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551348"
---
# <a name="accesspermission"></a>акцесспермиссион

Описывает список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса. Этот список ACL используется только приложениями, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Remarks

Это **\_ двоичное значение reg** . Он содержит данные, описывающие список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса. При получении запроса на подключение к существующему объекту этого класса ACL проверяется с помощью вызываемого приложения при олицетворении вызывающего. Если проверка доступа завершается сбоем, подключение запрещено. Если это именованное значение не существует, список ACL [**дефаултакцесспермиссион**](defaultaccesspermission.md) проверяется, чтобы определить, должно ли быть разрешено подключение.

Для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) или не используют интерфейс [**Иглобалоптионс**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) для указания AppID, исполняемый файл двоичного приложения должен быть сопоставлен с AppID приложения, как описано в [**AppID**](appid.md). Это необходимо для того, чтобы COM мог нахождение идентификатора AppID приложения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**дефаултакцесспермиссион**](defaultaccesspermission.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 