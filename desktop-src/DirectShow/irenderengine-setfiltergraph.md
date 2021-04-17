---
description: Метод Сетфилтерграф задает граф фильтра для использования подсистемой подготовки отчетов.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Метод Ирендеренгине:: Сетфилтерграф (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680038"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="ae3ed-103">Метод Ирендеренгине:: Сетфилтерграф</span><span class="sxs-lookup"><span data-stu-id="ae3ed-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="ae3ed-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-104">\[Deprecated.</span></span> <span data-ttu-id="ae3ed-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae3ed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ae3ed-106">`SetFilterGraph`Метод задает граф фильтра для использования подсистемой визуализации.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3ed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae3ed-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="ae3ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae3ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae3ed-109">*пфг*</span><span class="sxs-lookup"><span data-stu-id="ae3ed-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="ae3ed-110">Указатель на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae3ed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae3ed-111">Return value</span></span>

<span data-ttu-id="ae3ed-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ae3ed-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ae3ed-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ae3ed-113">Return code</span></span>                                                                                            | <span data-ttu-id="ae3ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ae3ed-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ae3ed-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3ed-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ae3ed-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="ae3ed-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3ed-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="ae3ed-118">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="ae3ed-119"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3ed-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="ae3ed-120">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae3ed-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae3ed-121">Remarks</span></span>

<span data-ttu-id="ae3ed-122">Большинству приложений не требуется вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="ae3ed-123">Более типично позволить подсистеме визуализации создать граф, вызвав метод [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="ae3ed-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="ae3ed-124">Этот метод завершается ошибкой, если обработчик визуализации уже имеет граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="ae3ed-125">Никогда не извлекайте указатель на граф фильтра, созданный одним модулем рендеринга, и затем используйте его в качестве параметра для этого метода в другом механизме отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="ae3ed-126">Это приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="ae3ed-127">Метод **коннектфронтенд** слезами любой существующий граф фильтра, но сохраняет тот же экземпляр диспетчера графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="ae3ed-128">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ae3ed-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae3ed-129">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae3ed-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ae3ed-130">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ae3ed-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae3ed-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ae3ed-131">Requirements</span></span>



| <span data-ttu-id="ae3ed-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ae3ed-132">Requirement</span></span> | <span data-ttu-id="ae3ed-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ae3ed-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3ed-134">Header</span><span class="sxs-lookup"><span data-stu-id="ae3ed-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ae3ed-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3ed-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ae3ed-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae3ed-136">Library</span></span><br/> | <dl> <span data-ttu-id="ae3ed-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae3ed-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae3ed-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae3ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3ed-139">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="ae3ed-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="ae3ed-140">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ae3ed-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




