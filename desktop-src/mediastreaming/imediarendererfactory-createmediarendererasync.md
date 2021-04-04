---
title: Имедиарендерерфактори Креатемедиарендерерасинк, метод
description: Асинхронно создает новый экземпляр объекта, который реализует интерфейс Имедиарендерер, используя указанное уникальное имя устройства (УДН).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API потоковой передачи мультимедиа метода Креатемедиарендерерасинк
- API потоковой передачи мультимедиа метода Креатемедиарендерерасинк, интерфейс Имедиарендерерфактори
- API потоковой передачи мультимедиа интерфейса Имедиарендерерфактори, метод Креатемедиарендерерасинк
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790561"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="5f4ea-106">Метод Имедиарендерерфактори:: Креатемедиарендерерасинк</span><span class="sxs-lookup"><span data-stu-id="5f4ea-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="5f4ea-107">Асинхронно создает новый экземпляр объекта, который реализует интерфейс [**имедиарендерер**](imediarenderer.md) , используя указанное уникальное имя устройства (УДН).</span><span class="sxs-lookup"><span data-stu-id="5f4ea-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4ea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f4ea-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="5f4ea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f4ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4ea-110">*девицеидентифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f4ea-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4ea-111">Объект HSTRING, содержащий УДН, который идентифицирует устройство DLNA ДМР, для которого будет создан экземпляр [**имедиарендерер**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="5f4ea-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="5f4ea-112">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5f4ea-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4ea-113">Получает ссылку на объект [**креатемедиарендерероператион**](createmediarendereroperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="5f4ea-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4ea-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f4ea-114">Return value</span></span>

<span data-ttu-id="5f4ea-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5f4ea-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5f4ea-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5f4ea-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5f4ea-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5f4ea-117">Return code</span></span>                                                                          | <span data-ttu-id="5f4ea-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5f4ea-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5f4ea-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4ea-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5f4ea-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5f4ea-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5f4ea-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f4ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4ea-122">**имедиарендерерфактори**</span><span class="sxs-lookup"><span data-stu-id="5f4ea-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

