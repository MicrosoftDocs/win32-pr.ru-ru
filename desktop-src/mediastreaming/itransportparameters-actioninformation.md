---
title: Итранспортпараметерс Актионинформатион, метод
description: Получает интерфейс Имедиарендерерактионинформатион, который предоставляет сведения о том, какие методы в настоящее время можно вызывать в ДМР.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API потоковой передачи мультимедиа метода Актионинформатион
- API потоковой передачи мультимедиа метода Актионинформатион, интерфейс Итранспортпараметерс
- API потоковой передачи мультимедиа интерфейса Итранспортпараметерс, метод Актионинформатион
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069904"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="4cd66-106">Метод Итранспортпараметерс:: Актионинформатион</span><span class="sxs-lookup"><span data-stu-id="4cd66-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="4cd66-107">Получает интерфейс [**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) , который предоставляет сведения о том, какие методы в настоящее время можно вызывать в ДМР.</span><span class="sxs-lookup"><span data-stu-id="4cd66-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd66-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cd66-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="4cd66-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cd66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd66-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4cd66-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd66-111">Получает ссылку на интерфейс [**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="4cd66-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd66-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cd66-112">Return value</span></span>

<span data-ttu-id="4cd66-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4cd66-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4cd66-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4cd66-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4cd66-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4cd66-115">Return code</span></span>                                                                          | <span data-ttu-id="4cd66-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4cd66-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4cd66-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd66-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4cd66-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4cd66-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4cd66-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd66-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd66-120">**итранспортпараметерс**</span><span class="sxs-lookup"><span data-stu-id="4cd66-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

