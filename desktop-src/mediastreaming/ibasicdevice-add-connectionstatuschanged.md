---
title: Метод add_ConnectionStatusChanged Ибасикдевице
description: Регистрирует обработчик событий для события Коннектионстатусчанжед. | Метод add_ConnectionStatusChanged Ибасикдевице
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API потоковой передачи мультимедиа add_ConnectionStatusChanged метода
- API потоковой передачи add_ConnectionStatusChanged метода, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694056"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="bc6a4-107">Метод Ибасикдевице:: Add \_ коннектионстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="bc6a4-107">IBasicDevice::add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="bc6a4-108">Регистрирует обработчик событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6a4-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6a4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc6a4-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="bc6a4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc6a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6a4-111">*обработчик событий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc6a4-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6a4-112">Функция обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bc6a4-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="bc6a4-113">*токен* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bc6a4-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6a4-114">Ссылка на токен, который можно использовать для отмены регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="bc6a4-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6a4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc6a4-115">Return value</span></span>

<span data-ttu-id="bc6a4-116">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bc6a4-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bc6a4-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bc6a4-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bc6a4-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bc6a4-118">Return code</span></span>                                                                          | <span data-ttu-id="bc6a4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="bc6a4-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bc6a4-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bc6a4-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bc6a4-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bc6a4-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc6a4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc6a4-122">Remarks</span></span>

<span data-ttu-id="bc6a4-123">Чтобы отменить регистрацию обработчика событий, зарегистрированного этим методом, передайте значение *токена* методу [**Remove \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6a4-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc6a4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc6a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6a4-125">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="bc6a4-125">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

