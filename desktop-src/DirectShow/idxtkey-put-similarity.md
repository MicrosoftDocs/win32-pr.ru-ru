---
description: Метод "разместить \_ подобие" задает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'Идксткэй: метод ut_Similarity:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675808"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="0f0cb-105">Идксткэй: \_ метод сходства:p UT</span><span class="sxs-lookup"><span data-stu-id="0f0cb-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="0f0cb-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-106">\[Deprecated.</span></span> <span data-ttu-id="0f0cb-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f0cb-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f0cb-108">`put_Similarity`Метод задает диапазон цветовых данных, которые становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="0f0cb-109">При более высоких значениях более широкий диапазон похожих цветов является прозрачным.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="0f0cb-110">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0cb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f0cb-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0f0cb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f0cb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0cb-113">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f0cb-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0cb-114">Задает значение подобия.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-114">Specifies the similarity value.</span></span> <span data-ttu-id="0f0cb-115">Допустимый диапазон: от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0cb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f0cb-116">Return value</span></span>

<span data-ttu-id="0f0cb-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f0cb-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f0cb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f0cb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f0cb-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f0cb-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0f0cb-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f0cb-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f0cb-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f0cb-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0f0cb-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f0cb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0f0cb-123">Requirements</span></span>



| <span data-ttu-id="0f0cb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0f0cb-124">Requirement</span></span> | <span data-ttu-id="0f0cb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0f0cb-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="0f0cb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0f0cb-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f0cb-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f0cb-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f0cb-128">Library</span></span><br/> | <dl> <span data-ttu-id="0f0cb-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f0cb-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0cb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f0cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0cb-131">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="0f0cb-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="0f0cb-132">**Идксткэй::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="0f0cb-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




