---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Функция обратного вызова (реализованная приложением), которая вызывается объектом Дкскоре для событий уведомления.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987762"
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

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)