---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Функция обратного вызова (реализованная приложением), которая вызывается объектом Дкскоре для событий уведомления.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787104"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>Обратный вызов PFN_DXCORE_NOTIFICATION_CALLBACK

Функция обратного вызова (реализованная приложением), которая вызывается объектом Дкскоре для событий уведомления.

## <a name="syntax"></a>Синтаксис

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Параметры

### <a name="notificationtype"></a>notificationType

Тип: **[дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md)**

Тип уведомления, представляющего этот вызов. Сведения о типах, допустимых для типов объектов, см. в таблице в [дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="object"></a>object

Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Объект [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) или [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) , создающий уведомление.

### <a name="context-in"></a>контекст [в]

Тип: **void \***

Указатель, который может быть `nullptr` , в объект, содержащий сведения о контексте.

## <a name="see-also"></a>См. также

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)