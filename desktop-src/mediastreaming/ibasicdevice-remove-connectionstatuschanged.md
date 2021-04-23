---
title: Метод remove_ConnectionStatusChanged Ибасикдевице
description: Отменяет регистрацию обработчика событий для события Коннектионстатусчанжед. | Метод remove_ConnectionStatusChanged Ибасикдевице
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API потоковой передачи мультимедиа remove_ConnectionStatusChanged метода
- API потоковой передачи remove_ConnectionStatusChanged метода, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703587"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="c1f98-107">Метод Ибасикдевице:: Remove \_ коннектионстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="c1f98-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="c1f98-108">Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f98-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f98-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1f98-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="c1f98-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1f98-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1f98-111">*токен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1f98-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1f98-112">Ссылка на маркер, полученный из метода [**Add \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md) при регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="c1f98-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1f98-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1f98-113">Return value</span></span>

<span data-ttu-id="c1f98-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c1f98-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c1f98-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c1f98-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c1f98-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c1f98-116">Return code</span></span>                                                                          | <span data-ttu-id="c1f98-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c1f98-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c1f98-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c1f98-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c1f98-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c1f98-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c1f98-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1f98-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f98-121">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="c1f98-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





