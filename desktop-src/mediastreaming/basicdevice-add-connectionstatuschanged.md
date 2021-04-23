---
title: Метод BasicDevice.add_ConnectionStatusChanged
description: Регистрирует обработчик событий для события Коннектионстатусчанжед. | Метод BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API потоковой передачи мультимедиа add_ConnectionStatusChanged метода
- API потоковой передачи add_ConnectionStatusChanged метода, интерфейс Басикдевице
- API потоковой передачи мультимедиа интерфейса Басикдевице, метод add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703569"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="93286-107">Басикдевице. Add \_ коннектионстатусчанжед, метод</span><span class="sxs-lookup"><span data-stu-id="93286-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="93286-108">Регистрирует обработчик событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="93286-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="93286-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93286-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="93286-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="93286-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93286-111">*обработчик событий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93286-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93286-112">Функция обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="93286-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="93286-113">*токен* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="93286-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="93286-114">Ссылка на токен, который можно использовать для отмены регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="93286-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93286-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93286-115">Return value</span></span>

<span data-ttu-id="93286-116">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="93286-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="93286-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="93286-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="93286-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="93286-118">Return code</span></span>                                                                          | <span data-ttu-id="93286-119">Описание</span><span class="sxs-lookup"><span data-stu-id="93286-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="93286-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="93286-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="93286-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="93286-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93286-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93286-122">Remarks</span></span>

<span data-ttu-id="93286-123">Чтобы отменить регистрацию обработчика событий, зарегистрированного этим методом, передайте значение *токена* методу [**Remove \_ коннектионстатусчанжед**](basicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="93286-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="93286-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93286-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="93286-125">[**басикдевице**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93286-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

