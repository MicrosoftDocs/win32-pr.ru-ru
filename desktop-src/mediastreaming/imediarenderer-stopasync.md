---
title: Имедиарендерер Стопасинк, метод
description: Указывает ДМР асинхронно закончить воспроизведение текущего содержимого. | Имедиарендерер Стопасинк, метод
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- API потоковой передачи мультимедиа метода Стопасинк
- API потоковой передачи мультимедиа метода Стопасинк, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Стопасинк
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914628"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="e52b8-107">Метод Имедиарендерер:: Стопасинк</span><span class="sxs-lookup"><span data-stu-id="e52b8-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="e52b8-108">Указывает ДМР асинхронно закончить воспроизведение текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="e52b8-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52b8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e52b8-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e52b8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e52b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e52b8-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e52b8-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e52b8-112">Получает ссылку на объект [**плайбаккоператион**](playbackoperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="e52b8-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e52b8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e52b8-113">Return value</span></span>

<span data-ttu-id="e52b8-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e52b8-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e52b8-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e52b8-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e52b8-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e52b8-116">Return code</span></span>                                                                          | <span data-ttu-id="e52b8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e52b8-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e52b8-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e52b8-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e52b8-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e52b8-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e52b8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e52b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52b8-121">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="e52b8-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





