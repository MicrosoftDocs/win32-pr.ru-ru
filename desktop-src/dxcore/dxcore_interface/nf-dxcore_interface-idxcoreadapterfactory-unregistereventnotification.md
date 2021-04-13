---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Отменяет регистрацию в уведомлении, которое вы ранее зарегистрировали для.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413453"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="31a4c-103">Метод Идкскореадаптерфактори:: Унрегистеревентнотификатион</span><span class="sxs-lookup"><span data-stu-id="31a4c-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="31a4c-104">Отменяет регистрацию в уведомлении, которое вы ранее зарегистрировали для.</span><span class="sxs-lookup"><span data-stu-id="31a4c-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="31a4c-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="31a4c-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31a4c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31a4c-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="31a4c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31a4c-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="31a4c-108">евенткукие</span><span class="sxs-lookup"><span data-stu-id="31a4c-108">eventCookie</span></span>

<span data-ttu-id="31a4c-109">Тип: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="31a4c-109">Type: **uint32_t**</span></span>

<span data-ttu-id="31a4c-110">Значение файла cookie (возвращается при вызове [идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)), представляющем ранее зарегистрированную регистрацию, для которой теперь нужно отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="31a4c-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="31a4c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31a4c-111">Returns</span></span>

<span data-ttu-id="31a4c-112">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="31a4c-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="31a4c-113">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="31a4c-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="31a4c-114">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="31a4c-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="31a4c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31a4c-115">Return value</span></span>|<span data-ttu-id="31a4c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="31a4c-116">Description</span></span>|
|-|-|
|<span data-ttu-id="31a4c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="31a4c-117">E_INVALIDARG</span></span>|<span data-ttu-id="31a4c-118">Значение *евенткукие* не является допустимым файлом cookie, представляющим прошлую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="31a4c-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="31a4c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31a4c-119">Remarks</span></span>

<span data-ttu-id="31a4c-120">**Унрегистеревентнотификатион** возвращает только после завершения всех обратных вызовов и ожидающих выполнения для этой регистрации.</span><span class="sxs-lookup"><span data-stu-id="31a4c-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="31a4c-121">Дкскоре гарантирует, что для этой регистрации не будут выполняться новые обратные вызовы после возвращения **унрегистеревентнотификатион** .</span><span class="sxs-lookup"><span data-stu-id="31a4c-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="31a4c-122">Однако во избежание взаимоблокировки при вызове **унрегистеревентнотификатион** из функции обратного вызова **унрегистеревентнотификатион** не ждет завершения активного обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="31a4c-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31a4c-123">Перед уничтожением объекта Дкскоре, представленного аргументом *дкскореобжект* , переданным в [Идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), необходимо использовать значение cookie для отмены регистрации этого объекта из уведомлений путем вызова **унрегистеревентнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="31a4c-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="31a4c-124">Если этого не сделать, то при обнаружении ситуации будет создано неустранимое исключение.</span><span class="sxs-lookup"><span data-stu-id="31a4c-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="31a4c-125">После отмены регистрации значения cookie это значение может быть возвращено последующей регистрацией.</span><span class="sxs-lookup"><span data-stu-id="31a4c-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="31a4c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31a4c-126">See also</span></span>

<span data-ttu-id="31a4c-127">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Использование DXCore для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="31a4c-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>