---
title: Плайбаккоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной одним из методов воспроизведения Медиарендерер.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Плайбаккоператион
- API потоковой передачи мультимедиа интерфейса Плайбаккоператион, метод Results
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411555"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="99d4b-106">Плайбаккоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="99d4b-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="99d4b-107">Возвращает результаты асинхронной операции, запущенной одним из методов воспроизведения [**медиарендерер**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="99d4b-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d4b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99d4b-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="99d4b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99d4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99d4b-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="99d4b-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="99d4b-111">Результат операции.</span><span class="sxs-lookup"><span data-stu-id="99d4b-111">The result of the operation.</span></span> <span data-ttu-id="99d4b-112">Значение 0 указывает, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="99d4b-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="99d4b-113">Другие значения зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="99d4b-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99d4b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99d4b-114">Return value</span></span>

<span data-ttu-id="99d4b-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="99d4b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="99d4b-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="99d4b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="99d4b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="99d4b-117">Return code</span></span>                                                                          | <span data-ttu-id="99d4b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="99d4b-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="99d4b-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="99d4b-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="99d4b-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="99d4b-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99d4b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99d4b-121">Remarks</span></span>

<span data-ttu-id="99d4b-122">Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](playbackoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="99d4b-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="99d4b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99d4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d4b-124">**плайбаккоператион**</span><span class="sxs-lookup"><span data-stu-id="99d4b-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





