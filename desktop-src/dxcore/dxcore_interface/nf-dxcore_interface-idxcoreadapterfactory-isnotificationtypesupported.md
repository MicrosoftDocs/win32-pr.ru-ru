---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Определяет, поддерживается ли указанный тип уведомлений операционной системой (ОС).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338585"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="3be8f-103">Метод Идкскореадаптерфактори:: Иснотификатионтипесуппортед</span><span class="sxs-lookup"><span data-stu-id="3be8f-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="3be8f-104">Определяет, поддерживается ли указанный тип уведомлений операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="3be8f-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="3be8f-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="3be8f-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3be8f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3be8f-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="3be8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3be8f-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="3be8f-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="3be8f-108">notificationType</span></span>

<span data-ttu-id="3be8f-109">Тип: **[дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="3be8f-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="3be8f-110">Тип уведомления, для которого запрашиваются сведения о поддержке.</span><span class="sxs-lookup"><span data-stu-id="3be8f-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="3be8f-111">Сведения о типах уведомлений см. в таблице в [дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="3be8f-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="3be8f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3be8f-112">Returns</span></span>

<span data-ttu-id="3be8f-113">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="3be8f-113">Type: **bool**</span></span>

<span data-ttu-id="3be8f-114">Возвращает значение,  `true`   Если тип уведомления поддерживается системой.</span><span class="sxs-lookup"><span data-stu-id="3be8f-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="3be8f-115">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="3be8f-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be8f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3be8f-116">Remarks</span></span>

<span data-ttu-id="3be8f-117">Можно вызвать **иснотификатионтипесуппортед** , чтобы определить, известен ли данный тип уведомления данной версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3be8f-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="3be8f-118">Например, тип уведомления, представленный в определенной версии Windows, неизвестен предыдущим версиям Windows.</span><span class="sxs-lookup"><span data-stu-id="3be8f-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="3be8f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3be8f-119">See also</span></span>

<span data-ttu-id="3be8f-120">[Идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="3be8f-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>