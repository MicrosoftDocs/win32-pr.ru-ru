---
title: Медиарендерер. Паусеасинк, метод
description: Указывает ДМР асинхронно приостановить воспроизведение текущего содержимого. | Медиарендерер. Паусеасинк, метод
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API потоковой передачи мультимедиа метода Паусеасинк
- API потоковой передачи мультимедиа метода Паусеасинк, интерфейс Медиарендерер
- API потоковой передачи мультимедиа интерфейса Медиарендерер, метод Паусеасинк
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713429"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="646d5-107">Медиарендерер. Паусеасинк, метод</span><span class="sxs-lookup"><span data-stu-id="646d5-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="646d5-108">Указывает ДМР асинхронно приостановить воспроизведение текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="646d5-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="646d5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="646d5-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="646d5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="646d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646d5-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="646d5-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="646d5-112">Получает ссылку на объект [**плайбаккоператион**](playbackoperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="646d5-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646d5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="646d5-113">Return value</span></span>

<span data-ttu-id="646d5-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="646d5-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="646d5-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="646d5-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="646d5-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="646d5-116">Return code</span></span>                                                                          | <span data-ttu-id="646d5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="646d5-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="646d5-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="646d5-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="646d5-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="646d5-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="646d5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="646d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646d5-121">**медиарендерер**</span><span class="sxs-lookup"><span data-stu-id="646d5-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





