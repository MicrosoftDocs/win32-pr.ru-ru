---
description: Метод Енаблетранситионс включает или отключает все переходы на временной шкале.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Метод Иамтимелине:: Енаблетранситионс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651787"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="a0c51-103">Метод Иамтимелине:: Енаблетранситионс</span><span class="sxs-lookup"><span data-stu-id="a0c51-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="a0c51-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a0c51-104">\[Deprecated.</span></span> <span data-ttu-id="a0c51-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0c51-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0c51-106">`EnableTransitions`Метод включает или отключает все переходы на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="a0c51-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="a0c51-107">Если переходы отключены, модули подготовки отчетов обрабатывают их как «быстрые»; Это значит, что отображаемые выходные данные быстро переходят с одной записи на другую.</span><span class="sxs-lookup"><span data-stu-id="a0c51-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="a0c51-108">Точка обрезки по умолчанию находится в середине до длительности перехода.</span><span class="sxs-lookup"><span data-stu-id="a0c51-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="a0c51-109">Можно изменить точку вырезания, вызвав метод [**иамтимелинетранс:: сеткутпоинт**](iamtimelinetrans-setcutpoint.md) для перехода.</span><span class="sxs-lookup"><span data-stu-id="a0c51-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="a0c51-110">Отключенные переходы не удаляются с временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="a0c51-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c51-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0c51-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="a0c51-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0c51-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0c51-113">*фенаблед*</span><span class="sxs-lookup"><span data-stu-id="a0c51-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="a0c51-114">Логическое значение, указывающее, следует ли включать или отключать переходы.</span><span class="sxs-lookup"><span data-stu-id="a0c51-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="a0c51-115">Если **значение равно true**, переходы включены.</span><span class="sxs-lookup"><span data-stu-id="a0c51-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="a0c51-116">Если **значение равно false**, переходы отключены.</span><span class="sxs-lookup"><span data-stu-id="a0c51-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0c51-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0c51-117">Return value</span></span>

<span data-ttu-id="a0c51-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0c51-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0c51-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0c51-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0c51-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0c51-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0c51-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a0c51-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0c51-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0c51-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0c51-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a0c51-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0c51-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a0c51-124">Requirements</span></span>



| <span data-ttu-id="a0c51-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a0c51-125">Requirement</span></span> | <span data-ttu-id="a0c51-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a0c51-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c51-127">Header</span><span class="sxs-lookup"><span data-stu-id="a0c51-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a0c51-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0c51-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0c51-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0c51-129">Library</span></span><br/> | <dl> <span data-ttu-id="a0c51-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0c51-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0c51-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0c51-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c51-132">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="a0c51-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="a0c51-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a0c51-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




