---
description: Метод Сеттимелинеобжект задает временную шкалу для использования обработчиком отрисовки.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'Метод Ирендеренгине:: Сеттимелинеобжект (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676021"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="b96f4-103">Метод Ирендеренгине:: Сеттимелинеобжект</span><span class="sxs-lookup"><span data-stu-id="b96f4-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="b96f4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b96f4-104">\[Deprecated.</span></span> <span data-ttu-id="b96f4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b96f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b96f4-106">`SetTimelineObject`Метод задает временную шкалу для использования обработчиком визуализации.</span><span class="sxs-lookup"><span data-stu-id="b96f4-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b96f4-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="b96f4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b96f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b96f4-109">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="b96f4-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="b96f4-110">Указатель на интерфейс [**иамтимелине**](iamtimeline.md) объекта временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="b96f4-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b96f4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b96f4-111">Return value</span></span>

<span data-ttu-id="b96f4-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b96f4-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b96f4-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b96f4-113">Return code</span></span>                                                                                            | <span data-ttu-id="b96f4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b96f4-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b96f4-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b96f4-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b96f4-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="b96f4-117"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="b96f4-118">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="b96f4-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="b96f4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="b96f4-120">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="b96f4-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="b96f4-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="b96f4-122">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="b96f4-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b96f4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b96f4-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b96f4-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b96f4-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b96f4-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b96f4-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b96f4-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b96f4-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b96f4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b96f4-127">Requirements</span></span>



| <span data-ttu-id="b96f4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b96f4-128">Requirement</span></span> | <span data-ttu-id="b96f4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b96f4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b96f4-130">Header</span><span class="sxs-lookup"><span data-stu-id="b96f4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b96f4-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b96f4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b96f4-132">Library</span></span><br/> | <dl> <span data-ttu-id="b96f4-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b96f4-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b96f4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b96f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96f4-135">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="b96f4-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="b96f4-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="b96f4-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




