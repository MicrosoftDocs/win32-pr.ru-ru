---
description: Метод Жетфилтерграф извлекает граф фильтра, созданный модулем визуализации, если таковой имеется.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Метод Ирендеренгине:: Жетфилтерграф (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674849"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="48f53-103">Метод Ирендеренгине:: Жетфилтерграф</span><span class="sxs-lookup"><span data-stu-id="48f53-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="48f53-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="48f53-104">\[Deprecated.</span></span> <span data-ttu-id="48f53-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="48f53-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="48f53-106">`GetFilterGraph`Метод получает граф фильтра, созданный модулем визуализации, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="48f53-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f53-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48f53-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="48f53-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="48f53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f53-109">*ппфг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="48f53-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f53-110">Получает указатель на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="48f53-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="48f53-111">Он получает значение **null** , если нет графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="48f53-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f53-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48f53-112">Return value</span></span>

<span data-ttu-id="48f53-113">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="48f53-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="48f53-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="48f53-114">Return code</span></span>                                                                                            | <span data-ttu-id="48f53-115">Описание</span><span class="sxs-lookup"><span data-stu-id="48f53-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="48f53-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="48f53-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="48f53-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="48f53-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="48f53-118"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="48f53-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="48f53-119">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="48f53-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="48f53-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="48f53-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="48f53-121">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="48f53-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="48f53-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48f53-122">Remarks</span></span>

<span data-ttu-id="48f53-123">Используйте метод [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) для создания внешнего интерфейса графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="48f53-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="48f53-124">Для предварительного просмотра используйте [**ирендеренгине:: рендераутпутпинс**](irenderengine-renderoutputpins.md) для завершения работы со графом.</span><span class="sxs-lookup"><span data-stu-id="48f53-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="48f53-125">Для выходных данных файла Подключите внешний интерфейс к комбинации модуля записи мультиплексора или файла.</span><span class="sxs-lookup"><span data-stu-id="48f53-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="48f53-126">Дополнительные сведения см. [в разделе Подготовка проекта к просмотру](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="48f53-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="48f53-127">Полученный граф можно запустить, приостановить, остановить и найти. Однако скорость воспроизведения не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="48f53-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="48f53-128">При возврате, если значение *\* Ппфг* не **равно NULL**, то интерфейс **играфбуилдер** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="48f53-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="48f53-129">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="48f53-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="48f53-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="48f53-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="48f53-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="48f53-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="48f53-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="48f53-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="48f53-133">Требования</span><span class="sxs-lookup"><span data-stu-id="48f53-133">Requirements</span></span>



| <span data-ttu-id="48f53-134">Требование</span><span class="sxs-lookup"><span data-stu-id="48f53-134">Requirement</span></span> | <span data-ttu-id="48f53-135">Значение</span><span class="sxs-lookup"><span data-stu-id="48f53-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48f53-136">Header</span><span class="sxs-lookup"><span data-stu-id="48f53-136">Header</span></span><br/>  | <dl> <span data-ttu-id="48f53-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f53-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="48f53-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48f53-138">Library</span></span><br/> | <dl> <span data-ttu-id="48f53-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48f53-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f53-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48f53-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f53-141">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="48f53-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="48f53-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="48f53-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




