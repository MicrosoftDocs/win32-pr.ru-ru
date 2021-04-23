---
description: Метод Сеткутсонли указывает, визуализируется ли переход в виде вырезания. Если да, то переход выполняется мгновенно в вырезанной точке. Если переход на новую версию занимает много времени, может потребоваться предварительный просмотр его в виде вырезанной области для ускорения просмотра.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Метод Иамтимелинетранс:: Сеткутсонли (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689520"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="d2726-105">Метод Иамтимелинетранс:: Сеткутсонли</span><span class="sxs-lookup"><span data-stu-id="d2726-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="d2726-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d2726-106">\[Deprecated.</span></span> <span data-ttu-id="d2726-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2726-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2726-108">`SetCutsOnly`Метод указывает, визуализируется ли переход в виде вырезания.</span><span class="sxs-lookup"><span data-stu-id="d2726-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="d2726-109">Если да, то переход выполняется мгновенно в вырезанной точке.</span><span class="sxs-lookup"><span data-stu-id="d2726-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="d2726-110">Если переход на новую версию занимает много времени, может потребоваться предварительный просмотр его в виде вырезанной области для ускорения просмотра.</span><span class="sxs-lookup"><span data-stu-id="d2726-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2726-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2726-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="d2726-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2726-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2726-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="d2726-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="d2726-114">Указывает, следует ли отображать переход в виде вырезания.</span><span class="sxs-lookup"><span data-stu-id="d2726-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="d2726-115">Если **значение равно true**, переход отображается как мгновенное вырезание.</span><span class="sxs-lookup"><span data-stu-id="d2726-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="d2726-116">Если **значение равно false**, переход отрисовывается в течение нормальной длительности.</span><span class="sxs-lookup"><span data-stu-id="d2726-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2726-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2726-117">Return value</span></span>

<span data-ttu-id="d2726-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2726-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2726-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2726-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2726-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2726-120">Remarks</span></span>

<span data-ttu-id="d2726-121">Отрисовка перехода в виде вырезания не совместима с обменом входными данными.</span><span class="sxs-lookup"><span data-stu-id="d2726-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="d2726-122">(См. [**иамтимелинетранс:: сетсвапинпутс**](iamtimelinetrans-setswapinputs.md).) При вызове `SetCutsOnly` со значением **true** он временно переопределяет параметр **сетсвапинпутс** .</span><span class="sxs-lookup"><span data-stu-id="d2726-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="d2726-123">Однако параметр «только быстрые» предназначен для предварительного просмотра, поэтому это ограничение не влияет на выходные данные, поэтому `SetCutsOnly` перед записью файла просто не забывайте вызывать его со значением **false** .</span><span class="sxs-lookup"><span data-stu-id="d2726-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="d2726-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d2726-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2726-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2726-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2726-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d2726-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2726-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d2726-127">Requirements</span></span>



| <span data-ttu-id="d2726-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d2726-128">Requirement</span></span> | <span data-ttu-id="d2726-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d2726-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2726-130">Header</span><span class="sxs-lookup"><span data-stu-id="d2726-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d2726-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2726-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2726-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2726-132">Library</span></span><br/> | <dl> <span data-ttu-id="d2726-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2726-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2726-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2726-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2726-135">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="d2726-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="d2726-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d2726-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




