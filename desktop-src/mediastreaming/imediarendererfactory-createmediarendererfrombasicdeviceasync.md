---
title: Имедиарендерерфактори Креатемедиарендерерфромбасикдевицеасинк, метод
description: Асинхронно создает новый экземпляр объекта, который реализует интерфейс Имедиарендерер, используя указанный интерфейс Ибасикдевице.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API потоковой передачи мультимедиа метода Креатемедиарендерерфромбасикдевицеасинк
- API потоковой передачи мультимедиа метода Креатемедиарендерерфромбасикдевицеасинк, интерфейс Имедиарендерерфактори
- API потоковой передачи мультимедиа интерфейса Имедиарендерерфактори, метод Креатемедиарендерерфромбасикдевицеасинк
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069905"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="1350f-106">Метод Имедиарендерерфактори:: Креатемедиарендерерфромбасикдевицеасинк</span><span class="sxs-lookup"><span data-stu-id="1350f-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="1350f-107">Асинхронно создает новый экземпляр объекта, который реализует интерфейс [**имедиарендерер**](imediarenderer.md) , используя указанный интерфейс [**ибасикдевице**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="1350f-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1350f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1350f-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="1350f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1350f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1350f-110">*басикдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1350f-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1350f-111">Указатель на интерфейс [**ибасикдевице**](ibasicdevice.md) , представляющий устройство, для которого будет создан экземпляр [**имедиарендерер**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="1350f-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="1350f-112">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1350f-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1350f-113">Получает ссылку на объект [**креатемедиарендерероператион**](createmediarendereroperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="1350f-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1350f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1350f-114">Return value</span></span>

<span data-ttu-id="1350f-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1350f-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1350f-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1350f-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1350f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1350f-117">Return code</span></span>                                                                          | <span data-ttu-id="1350f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1350f-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1350f-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1350f-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1350f-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1350f-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1350f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1350f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1350f-122">**имедиарендерерфактори**</span><span class="sxs-lookup"><span data-stu-id="1350f-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

