---
title: Метод BasicDevice.remove_ConnectionStatusChanged
description: Отменяет регистрацию обработчика событий для события Коннектионстатусчанжед. | Метод BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API потоковой передачи мультимедиа remove_ConnectionStatusChanged метода
- API потоковой передачи remove_ConnectionStatusChanged метода, интерфейс Басикдевице
- API потоковой передачи мультимедиа интерфейса Басикдевице, метод remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273564"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="34034-107">Басикдевице. Remove \_ коннектионстатусчанжед, метод</span><span class="sxs-lookup"><span data-stu-id="34034-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="34034-108">Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="34034-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="34034-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34034-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="34034-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="34034-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34034-111">*токен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34034-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34034-112">Ссылка на маркер, полученный из метода [**Add \_ коннектионстатусчанжед**](basicdevice-add-connectionstatuschanged.md) при регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="34034-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34034-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34034-113">Return value</span></span>

<span data-ttu-id="34034-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="34034-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="34034-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="34034-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="34034-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="34034-116">Return code</span></span>                                                                          | <span data-ttu-id="34034-117">Описание</span><span class="sxs-lookup"><span data-stu-id="34034-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="34034-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="34034-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="34034-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="34034-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="34034-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34034-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="34034-121">[**басикдевице**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34034-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

