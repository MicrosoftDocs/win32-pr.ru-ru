---
description: Метод размещения \_ алфарамп задает свойство alpha пандус. Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении. Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'Идксталфасеттер: метод ut_AlphaRamp:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689464"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="17b89-105">Идксталфасеттер::p UT \_ алфарамп метод</span><span class="sxs-lookup"><span data-stu-id="17b89-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="17b89-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="17b89-106">\[Deprecated.</span></span> <span data-ttu-id="17b89-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17b89-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17b89-108">`put_AlphaRamp`Метод задает свойство alpha пандус.</span><span class="sxs-lookup"><span data-stu-id="17b89-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="17b89-109">Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="17b89-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="17b89-110">Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.</span><span class="sxs-lookup"><span data-stu-id="17b89-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b89-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17b89-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="17b89-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="17b89-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b89-113">*Альфа-канал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17b89-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b89-114">Альфа-шкала в процентах.</span><span class="sxs-lookup"><span data-stu-id="17b89-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="17b89-115">Например, 1,0 — 100%.</span><span class="sxs-lookup"><span data-stu-id="17b89-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="17b89-116">Чтобы отключить это свойство, задайте отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="17b89-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b89-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17b89-117">Return value</span></span>

<span data-ttu-id="17b89-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="17b89-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17b89-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17b89-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b89-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17b89-120">Remarks</span></span>

<span data-ttu-id="17b89-121">Если для этого свойства задано неотрицательное значение, необходимо также отключить свойство Alpha, вызвав метод Set **\_ Alpha** с отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="17b89-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="17b89-122">В противном случае результат будет отображаться неправильно.</span><span class="sxs-lookup"><span data-stu-id="17b89-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="17b89-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="17b89-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17b89-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="17b89-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17b89-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="17b89-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17b89-126">Требования</span><span class="sxs-lookup"><span data-stu-id="17b89-126">Requirements</span></span>



| <span data-ttu-id="17b89-127">Требование</span><span class="sxs-lookup"><span data-stu-id="17b89-127">Requirement</span></span> | <span data-ttu-id="17b89-128">Значение</span><span class="sxs-lookup"><span data-stu-id="17b89-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b89-129">Header</span><span class="sxs-lookup"><span data-stu-id="17b89-129">Header</span></span><br/>  | <dl> <span data-ttu-id="17b89-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b89-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17b89-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17b89-131">Library</span></span><br/> | <dl> <span data-ttu-id="17b89-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17b89-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b89-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17b89-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b89-134">**Интерфейс Идксталфасеттер**</span><span class="sxs-lookup"><span data-stu-id="17b89-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="17b89-135">**Идксталфасеттер::p UT \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="17b89-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




