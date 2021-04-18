---
description: Метод "получить \_ подобие" извлекает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Метод Идксткэй:: get_Similarity (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675323"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="c5ecd-105">Метод Идксткэй:: Get \_ подобия</span><span class="sxs-lookup"><span data-stu-id="c5ecd-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="c5ecd-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-106">\[Deprecated.</span></span> <span data-ttu-id="c5ecd-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5ecd-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c5ecd-108">`get_Similarity`Метод извлекает диапазон цветовых данных, которые становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="c5ecd-109">При более высоких значениях более широкий диапазон похожих цветов является прозрачным.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="c5ecd-110">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ecd-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5ecd-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c5ecd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5ecd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ecd-113">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c5ecd-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ecd-114">Получает значение подобия.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ecd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5ecd-115">Return value</span></span>

<span data-ttu-id="c5ecd-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5ecd-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5ecd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ecd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5ecd-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5ecd-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c5ecd-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c5ecd-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5ecd-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c5ecd-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c5ecd-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5ecd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ecd-122">Requirements</span></span>



| <span data-ttu-id="c5ecd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ecd-123">Requirement</span></span> | <span data-ttu-id="c5ecd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ecd-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ecd-125">Header</span><span class="sxs-lookup"><span data-stu-id="c5ecd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ecd-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ecd-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c5ecd-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5ecd-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5ecd-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ecd-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ecd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ecd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ecd-130">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="c5ecd-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="c5ecd-131">**Идксткэй:: Get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="c5ecd-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




