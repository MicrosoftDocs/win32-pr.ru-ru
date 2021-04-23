---
title: Метод Ибасикдевице значков
description: Возвращает вектор интерфейсов Идевицеикон.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Значки. метод API потоковой передачи мультимедиа
- Значки. метод API потоковой передачи мультимедиа, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод значков
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789889"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="2eccd-106">Метод Ибасикдевице:: пиктограммы</span><span class="sxs-lookup"><span data-stu-id="2eccd-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="2eccd-107">Возвращает вектор интерфейсов [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="2eccd-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eccd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eccd-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="2eccd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eccd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eccd-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2eccd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eccd-111">Получает перечисляемую коллекцию указателей интерфейса [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="2eccd-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eccd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eccd-112">Return value</span></span>

<span data-ttu-id="2eccd-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2eccd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2eccd-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2eccd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2eccd-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2eccd-115">Return code</span></span>                                                                          | <span data-ttu-id="2eccd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2eccd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2eccd-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2eccd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2eccd-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2eccd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2eccd-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eccd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eccd-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="2eccd-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

