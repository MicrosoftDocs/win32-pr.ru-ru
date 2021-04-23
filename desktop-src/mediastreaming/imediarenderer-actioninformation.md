---
title: Имедиарендерер Актионинформатион, метод
description: Извлекает сведения о том, какие методы в данный момент можно вызывать в ДМР.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API потоковой передачи мультимедиа метода Актионинформатион
- API потоковой передачи мультимедиа метода Актионинформатион, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Актионинформатион
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069919"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="75f5c-106">Метод Имедиарендерер:: Актионинформатион</span><span class="sxs-lookup"><span data-stu-id="75f5c-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="75f5c-107">Извлекает сведения о том, какие методы в данный момент можно вызывать в ДМР.</span><span class="sxs-lookup"><span data-stu-id="75f5c-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f5c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75f5c-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="75f5c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="75f5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f5c-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75f5c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5c-111">Получает ссылку на интерфейс [**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="75f5c-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f5c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75f5c-112">Return value</span></span>

<span data-ttu-id="75f5c-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75f5c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75f5c-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75f5c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75f5c-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75f5c-115">Return code</span></span>                                                                          | <span data-ttu-id="75f5c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="75f5c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="75f5c-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="75f5c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="75f5c-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="75f5c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="75f5c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75f5c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f5c-120">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="75f5c-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

