---
description: Метод Сетрендерранже задает диапазон времени для отрисовки на временной шкале. Объекты, находящиеся за пределами указанного диапазона, не подготавливаются к просмотру, и ресурсы не выделяются для них.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'Метод Ирендеренгине:: Сетрендерранже (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676024"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="f9fab-104">Метод Ирендеренгине:: Сетрендерранже</span><span class="sxs-lookup"><span data-stu-id="f9fab-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="f9fab-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f9fab-105">\[Deprecated.</span></span> <span data-ttu-id="f9fab-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9fab-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9fab-107">`SetRenderRange`Метод задает диапазон времени для отрисовки на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="f9fab-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="f9fab-108">Объекты, находящиеся за пределами указанного диапазона, не подготавливаются к просмотру, и ресурсы не выделяются для них.</span><span class="sxs-lookup"><span data-stu-id="f9fab-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fab-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9fab-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="f9fab-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9fab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fab-111">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="f9fab-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fab-112">Время начала (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="f9fab-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f9fab-113">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="f9fab-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fab-114">Время окончания (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="f9fab-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fab-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9fab-115">Return value</span></span>

<span data-ttu-id="f9fab-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="f9fab-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f9fab-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f9fab-117">Return code</span></span>                                                                                            | <span data-ttu-id="f9fab-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f9fab-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f9fab-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fab-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f9fab-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f9fab-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="f9fab-121"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fab-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="f9fab-122">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="f9fab-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9fab-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9fab-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9fab-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f9fab-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9fab-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9fab-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9fab-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f9fab-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9fab-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f9fab-127">Requirements</span></span>



| <span data-ttu-id="f9fab-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f9fab-128">Requirement</span></span> | <span data-ttu-id="f9fab-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f9fab-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fab-130">Header</span><span class="sxs-lookup"><span data-stu-id="f9fab-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f9fab-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fab-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9fab-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f9fab-132">Library</span></span><br/> | <dl> <span data-ttu-id="f9fab-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9fab-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fab-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9fab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fab-135">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="f9fab-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f9fab-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f9fab-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




