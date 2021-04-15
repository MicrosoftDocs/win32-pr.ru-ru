---
description: Метод Жетграупаутпутпин получает выходной ПИН-код для указанной группы.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Метод Ирендеренгине:: Жетграупаутпутпин (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675928"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="1ec78-103">Метод Ирендеренгине:: Жетграупаутпутпин</span><span class="sxs-lookup"><span data-stu-id="1ec78-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="1ec78-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1ec78-104">\[Deprecated.</span></span> <span data-ttu-id="1ec78-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ec78-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1ec78-106">`GetGroupOutputPin`Метод получает выходной ПИН-код для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="1ec78-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec78-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="1ec78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec78-109">*Группа*</span><span class="sxs-lookup"><span data-stu-id="1ec78-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec78-110">Отсчитываемый от нуля индекс, указывающий группу.</span><span class="sxs-lookup"><span data-stu-id="1ec78-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="1ec78-111">*ппрендерпин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1ec78-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec78-112">Получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="1ec78-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec78-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec78-113">Return value</span></span>

<span data-ttu-id="1ec78-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ec78-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ec78-115">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="1ec78-115">Possible values include the following:</span></span>



| <span data-ttu-id="1ec78-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ec78-116">Return code</span></span>                                                                                                  | <span data-ttu-id="1ec78-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1ec78-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ec78-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="1ec78-119">Группа не имеет выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1ec78-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="1ec78-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="1ec78-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1ec78-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1ec78-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="1ec78-123">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="1ec78-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1ec78-124"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="1ec78-125">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="1ec78-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="1ec78-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="1ec78-127">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="1ec78-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="1ec78-128"><dt>**\_модуль подготовки \_ отчетов \_ не \_ работает**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="1ec78-129">Не удалось выполнить операцию, так как проект не был успешно визуализирован.</span><span class="sxs-lookup"><span data-stu-id="1ec78-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1ec78-130"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="1ec78-131">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1ec78-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="1ec78-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ec78-132">Remarks</span></span>

<span data-ttu-id="1ec78-133">Перед вызовом этого метода вызовите [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) , чтобы создать внешний интерфейс графа.</span><span class="sxs-lookup"><span data-stu-id="1ec78-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="1ec78-134">Каждая группа представляет один поток мультимедиа, а внешний интерфейс имеет соответствующий ПИН-код вывода.</span><span class="sxs-lookup"><span data-stu-id="1ec78-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="1ec78-135">Этот метод можно использовать для создания области отрисовки графа, записывающего файлы.</span><span class="sxs-lookup"><span data-stu-id="1ec78-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="1ec78-136">Подключите выходные контакты к фильтрам мультиплексора и фильтрам записи файлов.</span><span class="sxs-lookup"><span data-stu-id="1ec78-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="1ec78-137">Дополнительные сведения см. [в разделе Подготовка проекта к просмотру](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="1ec78-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="1ec78-138">Для предварительного просмотра не нужно вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="1ec78-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="1ec78-139">Просто вызовите **коннектфронтенд** , а затем [**Ирендеренгине:: рендераутпутпинс**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="1ec78-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="1ec78-140">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **Ипин** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="1ec78-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="1ec78-141">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="1ec78-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1ec78-142">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1ec78-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ec78-143">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ec78-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ec78-144">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1ec78-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ec78-145">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec78-145">Requirements</span></span>



| <span data-ttu-id="1ec78-146">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec78-146">Requirement</span></span> | <span data-ttu-id="1ec78-147">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec78-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec78-148">Header</span><span class="sxs-lookup"><span data-stu-id="1ec78-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec78-149"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ec78-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ec78-150">Library</span></span><br/> | <dl> <span data-ttu-id="1ec78-151"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ec78-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec78-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ec78-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec78-153">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="1ec78-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="1ec78-154">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1ec78-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




