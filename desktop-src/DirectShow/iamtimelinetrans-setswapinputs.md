---
description: Метод Сетсвапинпутс указывает, меняются ли входные данные перехода.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Метод Иамтимелинетранс:: Сетсвапинпутс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689340"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="88c9a-103">Метод Иамтимелинетранс:: Сетсвапинпутс</span><span class="sxs-lookup"><span data-stu-id="88c9a-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="88c9a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="88c9a-104">\[Deprecated.</span></span> <span data-ttu-id="88c9a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88c9a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88c9a-106">`SetSwapInputs`Метод указывает, меняются ли входные данные перехода.</span><span class="sxs-lookup"><span data-stu-id="88c9a-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="88c9a-107">По умолчанию переход проходит от состава всех слоев с низким приоритетом до слоя, в котором находится переход.</span><span class="sxs-lookup"><span data-stu-id="88c9a-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="88c9a-108">Эту прогрессию можно отменить, чтобы переход выполнялся с слоя, где он находится в составе слоев с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="88c9a-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="88c9a-109">Дополнительные сведения см. в разделе [направление перехода](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="88c9a-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88c9a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88c9a-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="88c9a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="88c9a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c9a-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="88c9a-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="88c9a-113">Указывает, будут ли входные данные перепутаны.</span><span class="sxs-lookup"><span data-stu-id="88c9a-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="88c9a-114">Если **значение равно false**, переход проходит от составного набора всех уровней с низким приоритетом до слоя перехода.</span><span class="sxs-lookup"><span data-stu-id="88c9a-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="88c9a-115">Если **значение равно true**, переход проходит в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="88c9a-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c9a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88c9a-116">Return value</span></span>

<span data-ttu-id="88c9a-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88c9a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88c9a-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88c9a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88c9a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88c9a-119">Remarks</span></span>

<span data-ttu-id="88c9a-120">Этот метод не изменяет направление визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="88c9a-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="88c9a-121">Например, очистка слева направо будет по-прежнему идти слева направо.</span><span class="sxs-lookup"><span data-stu-id="88c9a-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="88c9a-122">Чтобы изменить направление, задайте свойство **Progress** с помощью интерфейса [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="88c9a-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="88c9a-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="88c9a-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88c9a-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="88c9a-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88c9a-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="88c9a-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88c9a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="88c9a-126">Requirements</span></span>



| <span data-ttu-id="88c9a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="88c9a-127">Requirement</span></span> | <span data-ttu-id="88c9a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="88c9a-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88c9a-129">Header</span><span class="sxs-lookup"><span data-stu-id="88c9a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="88c9a-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c9a-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88c9a-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88c9a-131">Library</span></span><br/> | <dl> <span data-ttu-id="88c9a-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88c9a-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c9a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88c9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c9a-134">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="88c9a-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="88c9a-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="88c9a-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




