---
description: Метод Get \_ KeyType Извлекает тип ключа.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Метод Идксткэй:: get_KeyType (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675327"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="725fa-103">Метод Идксткэй:: Get \_ KeyType</span><span class="sxs-lookup"><span data-stu-id="725fa-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="725fa-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="725fa-104">\[Deprecated.</span></span> <span data-ttu-id="725fa-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="725fa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="725fa-106">`get_KeyType`Метод получает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="725fa-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="725fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="725fa-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="725fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="725fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725fa-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="725fa-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="725fa-110">Получает одно из следующих значений перечисления.</span><span class="sxs-lookup"><span data-stu-id="725fa-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="725fa-111">Значение</span><span class="sxs-lookup"><span data-stu-id="725fa-111">Value</span></span>             | <span data-ttu-id="725fa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="725fa-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="725fa-113">ДКСТКЭЙ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="725fa-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="725fa-114">Ключ чрома.</span><span class="sxs-lookup"><span data-stu-id="725fa-114">Chroma key.</span></span> <span data-ttu-id="725fa-115">(Ключ для значения RGB.)</span><span class="sxs-lookup"><span data-stu-id="725fa-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="725fa-116">ДКСТКЭЙ \_ нонред</span><span class="sxs-lookup"><span data-stu-id="725fa-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="725fa-117">Ключ нонред.</span><span class="sxs-lookup"><span data-stu-id="725fa-117">Nonred key.</span></span> <span data-ttu-id="725fa-118">(Делает прозрачными синие и зеленые области.)</span><span class="sxs-lookup"><span data-stu-id="725fa-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="725fa-119">\_светимость дксткэй</span><span class="sxs-lookup"><span data-stu-id="725fa-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="725fa-120">Ключ освещенности.</span><span class="sxs-lookup"><span data-stu-id="725fa-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="725fa-121">ДКСТКЭЙ \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="725fa-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="725fa-122">Ключ по значению альфа.</span><span class="sxs-lookup"><span data-stu-id="725fa-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="725fa-123">оттенок ДКСТКЭЙ \_</span><span class="sxs-lookup"><span data-stu-id="725fa-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="725fa-124">Ключ с оттенокм.</span><span class="sxs-lookup"><span data-stu-id="725fa-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725fa-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="725fa-125">Return value</span></span>

<span data-ttu-id="725fa-126">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="725fa-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="725fa-127">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="725fa-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="725fa-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="725fa-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="725fa-129">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="725fa-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="725fa-130">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="725fa-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="725fa-131">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="725fa-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="725fa-132">Требования</span><span class="sxs-lookup"><span data-stu-id="725fa-132">Requirements</span></span>



| <span data-ttu-id="725fa-133">Требование</span><span class="sxs-lookup"><span data-stu-id="725fa-133">Requirement</span></span> | <span data-ttu-id="725fa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="725fa-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="725fa-135">Header</span><span class="sxs-lookup"><span data-stu-id="725fa-135">Header</span></span><br/>  | <dl> <span data-ttu-id="725fa-136"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="725fa-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="725fa-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="725fa-137">Library</span></span><br/> | <dl> <span data-ttu-id="725fa-138"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="725fa-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725fa-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="725fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725fa-140">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="725fa-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




