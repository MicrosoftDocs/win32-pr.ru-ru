---
description: Метод «вставить \_ KeyType» указывает тип ключа.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'Идксткэй: метод ut_KeyType:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675318"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="11882-103">Идксткэй::p \_ метода UT KeyType</span><span class="sxs-lookup"><span data-stu-id="11882-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="11882-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="11882-104">\[Deprecated.</span></span> <span data-ttu-id="11882-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11882-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="11882-106">`put_KeyType`Метод задает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="11882-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="11882-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11882-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="11882-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11882-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11882-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11882-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11882-110">Указывает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="11882-110">Specifies the key type.</span></span> <span data-ttu-id="11882-111">Этот параметр должен быть одним из следующих значений перечисления.</span><span class="sxs-lookup"><span data-stu-id="11882-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="11882-112">Значение</span><span class="sxs-lookup"><span data-stu-id="11882-112">Value</span></span>             | <span data-ttu-id="11882-113">Описание</span><span class="sxs-lookup"><span data-stu-id="11882-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="11882-114">ДКСТКЭЙ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="11882-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="11882-115">Ключ чрома.</span><span class="sxs-lookup"><span data-stu-id="11882-115">Chroma key.</span></span> <span data-ttu-id="11882-116">(Ключ для значения RGB.)</span><span class="sxs-lookup"><span data-stu-id="11882-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="11882-117">ДКСТКЭЙ \_ нонред</span><span class="sxs-lookup"><span data-stu-id="11882-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="11882-118">Ключ нонред.</span><span class="sxs-lookup"><span data-stu-id="11882-118">Nonred key.</span></span> <span data-ttu-id="11882-119">(Делает прозрачными синие и зеленые области.)</span><span class="sxs-lookup"><span data-stu-id="11882-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="11882-120">\_светимость дксткэй</span><span class="sxs-lookup"><span data-stu-id="11882-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="11882-121">Ключ освещенности.</span><span class="sxs-lookup"><span data-stu-id="11882-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="11882-122">ДКСТКЭЙ \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="11882-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="11882-123">Ключ по значению альфа.</span><span class="sxs-lookup"><span data-stu-id="11882-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="11882-124">оттенок ДКСТКЭЙ \_</span><span class="sxs-lookup"><span data-stu-id="11882-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="11882-125">Ключ с оттенокм.</span><span class="sxs-lookup"><span data-stu-id="11882-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11882-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11882-126">Return value</span></span>

<span data-ttu-id="11882-127">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="11882-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11882-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11882-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11882-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11882-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11882-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="11882-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="11882-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="11882-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="11882-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="11882-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11882-133">Требования</span><span class="sxs-lookup"><span data-stu-id="11882-133">Requirements</span></span>



| <span data-ttu-id="11882-134">Требование</span><span class="sxs-lookup"><span data-stu-id="11882-134">Requirement</span></span> | <span data-ttu-id="11882-135">Значение</span><span class="sxs-lookup"><span data-stu-id="11882-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11882-136">Header</span><span class="sxs-lookup"><span data-stu-id="11882-136">Header</span></span><br/>  | <dl> <span data-ttu-id="11882-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="11882-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="11882-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11882-138">Library</span></span><br/> | <dl> <span data-ttu-id="11882-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11882-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11882-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11882-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11882-141">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="11882-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




