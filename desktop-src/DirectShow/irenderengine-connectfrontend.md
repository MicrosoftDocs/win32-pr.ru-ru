---
description: Метод Коннектфронтенд создает внешний интерфейс графа фильтра из текущей временной шкалы.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Метод Ирендеренгине:: Коннектфронтенд (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675929"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="4cae2-103">Метод Ирендеренгине:: Коннектфронтенд</span><span class="sxs-lookup"><span data-stu-id="4cae2-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="4cae2-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4cae2-104">\[Deprecated.</span></span> <span data-ttu-id="4cae2-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4cae2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cae2-106">`ConnectFrontEnd`Метод создает внешний интерфейс графа фильтра из текущей временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="4cae2-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cae2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cae2-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="4cae2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cae2-108">Parameters</span></span>

<span data-ttu-id="4cae2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4cae2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cae2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cae2-110">Return value</span></span>

<span data-ttu-id="4cae2-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cae2-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4cae2-112">Возможные возвращаемые значения включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4cae2-112">Possible return values include the following:</span></span>



| <span data-ttu-id="4cae2-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4cae2-113">Return code</span></span>                                                                                                  | <span data-ttu-id="4cae2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4cae2-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cae2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="4cae2-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4cae2-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4cae2-117"><dt>**\_предупреждать \_ аутпутресет**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="4cae2-118">Часть графа отрисовки была удалена.</span><span class="sxs-lookup"><span data-stu-id="4cae2-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="4cae2-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="4cae2-120">Для этого модуля визуализации не задана временная шкала.</span><span class="sxs-lookup"><span data-stu-id="4cae2-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="4cae2-121"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="4cae2-122">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="4cae2-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4cae2-123"><dt>**\_модуль подготовки \_ отчетов \_ не \_ работает**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="4cae2-124">Не удалось выполнить операцию, так как проект не был успешно визуализирован.</span><span class="sxs-lookup"><span data-stu-id="4cae2-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4cae2-125"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="4cae2-126">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4cae2-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="4cae2-127"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="4cae2-128">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="4cae2-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="4cae2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cae2-129">Remarks</span></span>

<span data-ttu-id="4cae2-130">Этот метод не создает часть отрисовки графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="4cae2-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="4cae2-131">Приложение должно подключить выходные контакты на внешнем интерфейсе к нужным фильтрам отрисовки:</span><span class="sxs-lookup"><span data-stu-id="4cae2-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="4cae2-132">Для предварительного просмотра вызовите метод [**ирендеренгине:: рендераутпутпинс**](irenderengine-renderoutputpins.md) .</span><span class="sxs-lookup"><span data-stu-id="4cae2-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="4cae2-133">Чтобы вывести файл, вызовите [**ирендеренгине:: жетграупаутпутпин**](irenderengine-getgroupoutputpin.md) , чтобы получить выходной ПИН-код для каждой группы, а затем соедините контакты с фильтром мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="4cae2-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="4cae2-134">Если используется базовый механизм визуализации, то выходные сигналы на внешнем интерфейсе создают несжатые данные.</span><span class="sxs-lookup"><span data-stu-id="4cae2-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="4cae2-135">Если используется интеллектуальный механизм визуализации, то выходные данные создают сжатые.</span><span class="sxs-lookup"><span data-stu-id="4cae2-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="4cae2-136">При изменении временной шкалы после построения графа фильтра необходимо вызвать `ConnectFrontEnd` повторный вызов для перестроения внешнего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4cae2-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="4cae2-137">По возможности метод сохраняет часть графа отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4cae2-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="4cae2-138">Тем не менее, если добавить или удалить группу или изменить порядок групп, будет `ConnectFrontEnd` удалена визуализация, а приложение должно перестроиться.</span><span class="sxs-lookup"><span data-stu-id="4cae2-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="4cae2-139">Если метод удаляет часть отрисовки, возвращается \_ предупреждение \_ аутпутресет.</span><span class="sxs-lookup"><span data-stu-id="4cae2-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="4cae2-140">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4cae2-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cae2-141">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cae2-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4cae2-142">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4cae2-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cae2-143">Требования</span><span class="sxs-lookup"><span data-stu-id="4cae2-143">Requirements</span></span>



| <span data-ttu-id="4cae2-144">Требование</span><span class="sxs-lookup"><span data-stu-id="4cae2-144">Requirement</span></span> | <span data-ttu-id="4cae2-145">Значение</span><span class="sxs-lookup"><span data-stu-id="4cae2-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cae2-146">Header</span><span class="sxs-lookup"><span data-stu-id="4cae2-146">Header</span></span><br/>  | <dl> <span data-ttu-id="4cae2-147"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4cae2-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4cae2-148">Library</span></span><br/> | <dl> <span data-ttu-id="4cae2-149"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cae2-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cae2-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cae2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae2-151">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="4cae2-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="4cae2-152">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4cae2-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




