---
description: Метод Рендераутпутпинс создает часть предварительного просмотра графа фильтра.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Метод Ирендеренгине:: Рендераутпутпинс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676027"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="c51dc-103">Метод Ирендеренгине:: Рендераутпутпинс</span><span class="sxs-lookup"><span data-stu-id="c51dc-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="c51dc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c51dc-104">\[Deprecated.</span></span> <span data-ttu-id="c51dc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c51dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c51dc-106">`RenderOutputPins`Метод создает часть предварительного просмотра графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="c51dc-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c51dc-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="c51dc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c51dc-108">Parameters</span></span>

<span data-ttu-id="c51dc-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c51dc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c51dc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c51dc-110">Return value</span></span>

<span data-ttu-id="c51dc-111">Возвращает значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c51dc-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="c51dc-112">Возможные следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c51dc-112">The following are possible values:</span></span>



| <span data-ttu-id="c51dc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c51dc-113">Return code</span></span>                                                                                                  | <span data-ttu-id="c51dc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c51dc-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c51dc-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="c51dc-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c51dc-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c51dc-117"><dt>**\_звуковые файлы VFW S \_ \_ не \_ визуализируются**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="c51dc-118">Не удается воспроизвести аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="c51dc-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="c51dc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="c51dc-120">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="c51dc-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c51dc-121"><dt>**\_модуль подготовки \_ отчетов \_ не \_ работает**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="c51dc-122">Не удалось выполнить операцию, так как проект не был успешно визуализирован.</span><span class="sxs-lookup"><span data-stu-id="c51dc-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c51dc-123"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="c51dc-124">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c51dc-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="c51dc-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c51dc-125">Remarks</span></span>

<span data-ttu-id="c51dc-126">Перед вызовом этого метода вызовите [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) , чтобы создать внешний интерфейс графа.</span><span class="sxs-lookup"><span data-stu-id="c51dc-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="c51dc-127">Чтобы выполнить операцию, отличную от предварительной, не вызывайте этот метод.</span><span class="sxs-lookup"><span data-stu-id="c51dc-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="c51dc-128">Вместо этого вызовите [**ирендеренгине:: жетграупаутпутпин**](irenderengine-getgroupoutputpin.md) , чтобы получить указатели на выходные данные.</span><span class="sxs-lookup"><span data-stu-id="c51dc-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="c51dc-129">Если на компьютере пользователя нет звуковой платы, этот метод возвращает значение VFW \_ s \_ Audio \_ Not \_ rendered.</span><span class="sxs-lookup"><span data-stu-id="c51dc-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="c51dc-130">В этом случае не будет предварительного просмотра аудио, но на просмотр видео это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="c51dc-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="c51dc-131">Если закрепить из видеогруппы, этот метод создает окно видео.</span><span class="sxs-lookup"><span data-stu-id="c51dc-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="c51dc-132">Вызывающий поток должен отправлять сообщения, например, для перемещения окна или реагирования на щелчки мыши в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="c51dc-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="c51dc-133">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c51dc-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c51dc-134">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c51dc-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c51dc-135">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c51dc-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c51dc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c51dc-136">Requirements</span></span>



| <span data-ttu-id="c51dc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c51dc-137">Requirement</span></span> | <span data-ttu-id="c51dc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c51dc-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c51dc-139">Header</span><span class="sxs-lookup"><span data-stu-id="c51dc-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c51dc-140"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c51dc-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c51dc-141">Library</span></span><br/> | <dl> <span data-ttu-id="c51dc-142"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c51dc-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c51dc-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c51dc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51dc-144">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="c51dc-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="c51dc-145">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c51dc-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




