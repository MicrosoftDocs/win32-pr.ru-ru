---
title: Имедиарендерер Паусеасинк, метод
description: Указывает ДМР асинхронно приостановить воспроизведение текущего содержимого. | Имедиарендерер Паусеасинк, метод
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API потоковой передачи мультимедиа метода Паусеасинк
- API потоковой передачи мультимедиа метода Паусеасинк, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Паусеасинк
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713424"
---
# <a name="imediarendererpauseasync-method"></a><span data-ttu-id="894aa-107">Имедиарендерер: метод:P Аусеасинк</span><span class="sxs-lookup"><span data-stu-id="894aa-107">IMediaRenderer::PauseAsync method</span></span>

<span data-ttu-id="894aa-108">Указывает ДМР асинхронно приостановить воспроизведение текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="894aa-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="894aa-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="894aa-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="894aa-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="894aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894aa-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="894aa-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="894aa-112">Получает ссылку на объект [**плайбаккоператион**](playbackoperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="894aa-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894aa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="894aa-113">Return value</span></span>

<span data-ttu-id="894aa-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="894aa-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="894aa-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="894aa-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="894aa-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="894aa-116">Return code</span></span>                                                                          | <span data-ttu-id="894aa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="894aa-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="894aa-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="894aa-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="894aa-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="894aa-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="894aa-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="894aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894aa-121">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="894aa-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





