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
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="f354c-103">Обратный вызов PFN_DXCORE_NOTIFICATION_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f354c-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="f354c-104">Функция обратного вызова (реализованная приложением), которая вызывается объектом Дкскоре для событий уведомления.</span><span class="sxs-lookup"><span data-stu-id="f354c-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="f354c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f354c-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="f354c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f354c-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="f354c-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="f354c-107">notificationType</span></span>

<span data-ttu-id="f354c-108">Тип: **[дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="f354c-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="f354c-109">Тип уведомления, представляющего этот вызов.</span><span class="sxs-lookup"><span data-stu-id="f354c-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="f354c-110">Сведения о типах, допустимых для типов объектов, см. в таблице в [дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="f354c-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="f354c-111">object</span><span class="sxs-lookup"><span data-stu-id="f354c-111">object</span></span>

<span data-ttu-id="f354c-112">Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="f354c-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="f354c-113">Объект [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) или [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) , создающий уведомление.</span><span class="sxs-lookup"><span data-stu-id="f354c-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="f354c-114">контекст [в]</span><span class="sxs-lookup"><span data-stu-id="f354c-114">context [in]</span></span>

<span data-ttu-id="f354c-115">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="f354c-115">Type: **void\***</span></span>

<span data-ttu-id="f354c-116">Указатель, который может быть `nullptr` , в объект, содержащий сведения о контексте.</span><span class="sxs-lookup"><span data-stu-id="f354c-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="f354c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f354c-117">See also</span></span>

<span data-ttu-id="f354c-118">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f354c-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>