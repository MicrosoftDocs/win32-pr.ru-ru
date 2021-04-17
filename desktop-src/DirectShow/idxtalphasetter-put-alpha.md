---
description: Метод постановки \_ Alpha задает альфа-значение для всего изображения.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'Идксталфасеттер: метод ut_Alpha:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688995"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="af609-103">Идксталфасеттер::p \_ методу UT Alpha</span><span class="sxs-lookup"><span data-stu-id="af609-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="af609-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="af609-104">\[Deprecated.</span></span> <span data-ttu-id="af609-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af609-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="af609-106">`put_Alpha`Метод задает альфа-значение для всего изображения.</span><span class="sxs-lookup"><span data-stu-id="af609-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="af609-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af609-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="af609-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af609-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af609-109">*Альфа-канал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af609-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af609-110">Альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="af609-110">The alpha value.</span></span> <span data-ttu-id="af609-111">Это значение будет применено ко всему целевому образу.</span><span class="sxs-lookup"><span data-stu-id="af609-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="af609-112">Чтобы отключить это свойство, задайте отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="af609-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af609-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af609-113">Return value</span></span>

<span data-ttu-id="af609-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="af609-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af609-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af609-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af609-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af609-116">Remarks</span></span>

<span data-ttu-id="af609-117">Если для этого свойства задано неотрицательное значение, необходимо также отключить свойство alpha пандус, вызвав метод Set **\_ алфарамп** с отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="af609-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="af609-118">В противном случае результат будет отображаться неправильно.</span><span class="sxs-lookup"><span data-stu-id="af609-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="af609-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="af609-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="af609-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="af609-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="af609-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="af609-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af609-122">Требования</span><span class="sxs-lookup"><span data-stu-id="af609-122">Requirements</span></span>



| <span data-ttu-id="af609-123">Требование</span><span class="sxs-lookup"><span data-stu-id="af609-123">Requirement</span></span> | <span data-ttu-id="af609-124">Значение</span><span class="sxs-lookup"><span data-stu-id="af609-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af609-125">Header</span><span class="sxs-lookup"><span data-stu-id="af609-125">Header</span></span><br/>  | <dl> <span data-ttu-id="af609-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="af609-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="af609-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af609-127">Library</span></span><br/> | <dl> <span data-ttu-id="af609-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af609-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af609-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af609-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af609-130">**Интерфейс Идксталфасеттер**</span><span class="sxs-lookup"><span data-stu-id="af609-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="af609-131">**Идксталфасеттер::p UT \_ алфарамп**</span><span class="sxs-lookup"><span data-stu-id="af609-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




