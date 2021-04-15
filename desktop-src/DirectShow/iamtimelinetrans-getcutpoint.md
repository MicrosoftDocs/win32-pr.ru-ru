---
description: Метод Жеткутпоинт извлекает вырезанную точку.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Метод Иамтимелинетранс:: Жеткутпоинт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689449"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="16ed3-103">Метод Иамтимелинетранс:: Жеткутпоинт</span><span class="sxs-lookup"><span data-stu-id="16ed3-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="16ed3-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="16ed3-104">\[Deprecated.</span></span> <span data-ttu-id="16ed3-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16ed3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16ed3-106">`GetCutPoint`Метод извлекает вырезанную точку.</span><span class="sxs-lookup"><span data-stu-id="16ed3-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="16ed3-107">При отрисовке перехода в виде вырезанной точки обрезка — это время, когда переход переходит от одного источника к другому.</span><span class="sxs-lookup"><span data-stu-id="16ed3-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="16ed3-108">По умолчанию это значение представляет собой середину перехода.</span><span class="sxs-lookup"><span data-stu-id="16ed3-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="16ed3-109">Например, в переходе, охватывающем одну секунду, вырезанная точка по умолчанию составляет 0,5 секунд в процессе перехода.</span><span class="sxs-lookup"><span data-stu-id="16ed3-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ed3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16ed3-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="16ed3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="16ed3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ed3-112">*птлтиме*</span><span class="sxs-lookup"><span data-stu-id="16ed3-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="16ed3-113">Получает вырезанную точку относительно времени начала перехода, в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="16ed3-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ed3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16ed3-114">Return value</span></span>

<span data-ttu-id="16ed3-115">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="16ed3-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="16ed3-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="16ed3-116">Return code</span></span>                                                                               | <span data-ttu-id="16ed3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="16ed3-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16ed3-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="16ed3-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="16ed3-119">Не задана вырезанная точка.</span><span class="sxs-lookup"><span data-stu-id="16ed3-119">The cut point was not set.</span></span> <span data-ttu-id="16ed3-120">Возвращаемое значение является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16ed3-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="16ed3-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="16ed3-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="16ed3-122">Для вырезанной точки задано значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16ed3-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="16ed3-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="16ed3-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="16ed3-124">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="16ed3-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="16ed3-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16ed3-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16ed3-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="16ed3-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16ed3-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16ed3-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16ed3-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="16ed3-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16ed3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="16ed3-129">Requirements</span></span>



| <span data-ttu-id="16ed3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="16ed3-130">Requirement</span></span> | <span data-ttu-id="16ed3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="16ed3-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16ed3-132">Header</span><span class="sxs-lookup"><span data-stu-id="16ed3-132">Header</span></span><br/>  | <dl> <span data-ttu-id="16ed3-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="16ed3-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16ed3-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16ed3-134">Library</span></span><br/> | <dl> <span data-ttu-id="16ed3-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16ed3-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16ed3-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16ed3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ed3-137">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="16ed3-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="16ed3-138">**Иамтимелинетранс:: Сеткутпоинт**</span><span class="sxs-lookup"><span data-stu-id="16ed3-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="16ed3-139">**Иамтимелинетранс:: Жеткутсонли**</span><span class="sxs-lookup"><span data-stu-id="16ed3-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="16ed3-140">**Иамтимелине:: Транситионсенаблед**</span><span class="sxs-lookup"><span data-stu-id="16ed3-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="16ed3-141">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="16ed3-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




