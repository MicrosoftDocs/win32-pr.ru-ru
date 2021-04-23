---
description: 'Интерфейс Ирендеренгине визуализирует проект служб редактирования DirectShow (DES), создавая граф фильтра из временной шкалы. DES предоставляет два компонента, реализующих этот интерфейс: базовый механизм визуализации создает несжатые выходные данные.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Интерфейс Ирендеренгине (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679843"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="01724-103">Интерфейс Ирендеренгине</span><span class="sxs-lookup"><span data-stu-id="01724-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="01724-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="01724-104">\[Deprecated.</span></span> <span data-ttu-id="01724-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01724-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01724-106">`IRenderEngine`Интерфейс визуализирует проект [служб редактирования DirectShow](directshow-editing-services.md) (DES), создавая граф фильтра из временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="01724-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="01724-107">DES предоставляет два компонента, которые реализуют этот интерфейс:</span><span class="sxs-lookup"><span data-stu-id="01724-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="01724-108">*Базовый механизм визуализации* создает несжатые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="01724-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="01724-109">Вы можете использовать выходные данные для предварительного просмотра или направить его с помощью фильтров сжатия и записать в файл.</span><span class="sxs-lookup"><span data-stu-id="01724-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="01724-110">*Интеллектуальный модуль визуализации* создает сжатые выходные данные, используя *интеллектуальное* повторное сжатие.</span><span class="sxs-lookup"><span data-stu-id="01724-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="01724-111">При использовании интеллектуального сжатия исходный файл сжимается только в том случае, если его формат отличается от формата выходных данных.</span><span class="sxs-lookup"><span data-stu-id="01724-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="01724-112">Источник с соответствующим форматом записывается непосредственно в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="01724-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="01724-113">В зависимости от сценария интеллектуальное повторное сжатие может значительно повысить время визуализации.</span><span class="sxs-lookup"><span data-stu-id="01724-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="01724-114">Модуль интеллектуального просмотра также поддерживает интерфейс [**исмартрендеренгине**](ismartrenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="01724-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="01724-115">Хотя приложение может создать граф фильтра и передать его в механизм визуализации, типичным сценарием является создание графа фильтра модулем визуализации.</span><span class="sxs-lookup"><span data-stu-id="01724-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="01724-116">Построение графа является процессом, сооснованным на двух стадиях.</span><span class="sxs-lookup"><span data-stu-id="01724-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="01724-117">Сначала создайте интерфейс, вызвав метод [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="01724-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="01724-118">Затем подключите выходные контакты на внешнем интерфейсе к нужным фильтрам отрисовки:</span><span class="sxs-lookup"><span data-stu-id="01724-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="01724-119">Модули подготовки видео и звука для предварительного просмотра или</span><span class="sxs-lookup"><span data-stu-id="01724-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="01724-120">Программы сжатия, мультиплексоры и записи файлов для создания окончательных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="01724-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="01724-121">Элементы</span><span class="sxs-lookup"><span data-stu-id="01724-121">Members</span></span>

<span data-ttu-id="01724-122">Интерфейс **ирендеренгине** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01724-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01724-123">**Ирендеренгине** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="01724-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="01724-124">Методы</span><span class="sxs-lookup"><span data-stu-id="01724-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01724-125">Методы</span><span class="sxs-lookup"><span data-stu-id="01724-125">Methods</span></span>

<span data-ttu-id="01724-126">Интерфейс **ирендеренгине** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="01724-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="01724-127">Метод</span><span class="sxs-lookup"><span data-stu-id="01724-127">Method</span></span>                                                                             | <span data-ttu-id="01724-128">Описание</span><span class="sxs-lookup"><span data-stu-id="01724-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="01724-129">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="01724-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="01724-130">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="01724-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="01724-131">**коннектфронтенд**</span><span class="sxs-lookup"><span data-stu-id="01724-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="01724-132">Формирует внешний интерфейс графа фильтра из текущей временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="01724-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="01724-133">**Освобождения**</span><span class="sxs-lookup"><span data-stu-id="01724-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="01724-134">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="01724-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="01724-135">**досмартрекомпрессион**</span><span class="sxs-lookup"><span data-stu-id="01724-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="01724-136">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01724-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="01724-137">**Cap**</span><span class="sxs-lookup"><span data-stu-id="01724-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="01724-138">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="01724-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="01724-139">**жетфилтерграф**</span><span class="sxs-lookup"><span data-stu-id="01724-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="01724-140">Извлекает граф фильтра, созданный модулем подготовки отчетов, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="01724-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="01724-141">**жетграупаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="01724-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="01724-142">Получает выходной ПИН-код для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="01724-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="01724-143">**жеттимелинеобжект**</span><span class="sxs-lookup"><span data-stu-id="01724-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="01724-144">Извлекает временную шкалу, используемую подсистемой отрисовки в данный момент.</span><span class="sxs-lookup"><span data-stu-id="01724-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="01724-145">**жетвендорстринг**</span><span class="sxs-lookup"><span data-stu-id="01724-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="01724-146">Извлекает строку поставщика.</span><span class="sxs-lookup"><span data-stu-id="01724-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="01724-147">**рендераутпутпинс**</span><span class="sxs-lookup"><span data-stu-id="01724-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="01724-148">Создает часть предварительного просмотра графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="01724-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="01724-149">**скрапит**</span><span class="sxs-lookup"><span data-stu-id="01724-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="01724-150">Отменяет граф фильтра механизма визуализации и все связанные объекты.</span><span class="sxs-lookup"><span data-stu-id="01724-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="01724-151">**сетдинамикреконнектлевел**</span><span class="sxs-lookup"><span data-stu-id="01724-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="01724-152">Задает уровень динамического повторного подключения во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="01724-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="01724-153">**сетфилтерграф**</span><span class="sxs-lookup"><span data-stu-id="01724-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="01724-154">Задает граф фильтра для использования подсистемой подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="01724-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="01724-155">**сетинтерестранже**</span><span class="sxs-lookup"><span data-stu-id="01724-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="01724-156">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01724-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="01724-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="01724-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="01724-158">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01724-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="01724-159">**сетрендерранже**</span><span class="sxs-lookup"><span data-stu-id="01724-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="01724-160">Задает диапазон времени для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="01724-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="01724-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="01724-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="01724-162">Задает отображаемый диапазон времени в виде значения **типа Double**.</span><span class="sxs-lookup"><span data-stu-id="01724-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="01724-163">**сетсаурцеконнекткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="01724-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="01724-164">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01724-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="01724-165">**сетсаурценамевалидатион**</span><span class="sxs-lookup"><span data-stu-id="01724-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="01724-166">Указывает, каким способом модуль подготовки отчетов проверяет имена файлов.</span><span class="sxs-lookup"><span data-stu-id="01724-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="01724-167">**сеттимелинеобжект**</span><span class="sxs-lookup"><span data-stu-id="01724-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="01724-168">Задает временную шкалу для использования обработчиком визуализации.</span><span class="sxs-lookup"><span data-stu-id="01724-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="01724-169">**усеинсмартрекомпрессионграф**</span><span class="sxs-lookup"><span data-stu-id="01724-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="01724-170">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01724-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="01724-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01724-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01724-172">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="01724-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01724-173">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="01724-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01724-174">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="01724-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01724-175">Требования</span><span class="sxs-lookup"><span data-stu-id="01724-175">Requirements</span></span>



| <span data-ttu-id="01724-176">Требование</span><span class="sxs-lookup"><span data-stu-id="01724-176">Requirement</span></span> | <span data-ttu-id="01724-177">Значение</span><span class="sxs-lookup"><span data-stu-id="01724-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01724-178">Header</span><span class="sxs-lookup"><span data-stu-id="01724-178">Header</span></span><br/>  | <dl> <span data-ttu-id="01724-179"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="01724-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01724-180">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01724-180">Library</span></span><br/> | <dl> <span data-ttu-id="01724-181"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01724-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01724-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01724-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01724-183">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="01724-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
