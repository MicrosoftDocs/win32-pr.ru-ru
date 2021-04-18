---
description: 'Метод SetRenderRange2 задает диапазон времени для отрисовки на временной шкале. Этот метод эквивалентен Ирендеренгине:: Сетрендерранже, но принимает значения типа Double.'
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Метод Ирендеренгине:: SetRenderRange2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676023"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="6da70-104">Метод Ирендеренгине:: SetRenderRange2</span><span class="sxs-lookup"><span data-stu-id="6da70-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="6da70-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6da70-105">\[Deprecated.</span></span> <span data-ttu-id="6da70-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6da70-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6da70-107">`SetRenderRange2`Метод задает диапазон времени для отрисовки на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="6da70-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="6da70-108">Этот метод эквивалентен [**ирендеренгине:: сетрендерранже**](irenderengine-setrenderrange.md), но принимает значения типа **Double**.</span><span class="sxs-lookup"><span data-stu-id="6da70-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da70-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6da70-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="6da70-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6da70-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da70-111">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="6da70-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="6da70-112">Время начала в секундах.</span><span class="sxs-lookup"><span data-stu-id="6da70-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="6da70-113">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="6da70-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="6da70-114">Время окончания в секундах.</span><span class="sxs-lookup"><span data-stu-id="6da70-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da70-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6da70-115">Return value</span></span>

<span data-ttu-id="6da70-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="6da70-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="6da70-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6da70-117">Return code</span></span>                                                                                            | <span data-ttu-id="6da70-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6da70-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6da70-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6da70-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6da70-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6da70-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="6da70-121"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="6da70-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="6da70-122">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="6da70-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6da70-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6da70-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6da70-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="6da70-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6da70-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6da70-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6da70-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6da70-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6da70-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6da70-127">Requirements</span></span>



| <span data-ttu-id="6da70-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6da70-128">Requirement</span></span> | <span data-ttu-id="6da70-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6da70-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da70-130">Header</span><span class="sxs-lookup"><span data-stu-id="6da70-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6da70-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="6da70-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6da70-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6da70-132">Library</span></span><br/> | <dl> <span data-ttu-id="6da70-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6da70-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da70-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6da70-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da70-135">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="6da70-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="6da70-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="6da70-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




