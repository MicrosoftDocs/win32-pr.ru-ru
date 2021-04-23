---
description: Функция-посредник для метода Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: Функция IWICFormatConverter_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266145"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="28f40-103">Ивикформатконвертер \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="28f40-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="28f40-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="28f40-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28f40-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="28f40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28f40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f40-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="28f40-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-108">Тип: \**[**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="28f40-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="28f40-109">Указатель на этот объект [_ *ивикформатконвертер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="28f40-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="28f40-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28f40-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="28f40-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="28f40-112">Входной точечный рисунок для преобразования</span><span class="sxs-lookup"><span data-stu-id="28f40-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="28f40-113">_dstFormat \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="28f40-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-114">Тип: **рефвикпикселформатгуид**</span><span class="sxs-lookup"><span data-stu-id="28f40-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="28f40-115">Идентификатор GUID конечного формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="28f40-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="28f40-116">*дизеринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28f40-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-117">Тип: **[ **викбитмапдисертипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="28f40-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="28f40-118">[**Викбитмапдисертипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) , используемый для преобразования.</span><span class="sxs-lookup"><span data-stu-id="28f40-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="28f40-119">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28f40-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-120">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="28f40-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="28f40-121">Палитра, используемая для преобразования.</span><span class="sxs-lookup"><span data-stu-id="28f40-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="28f40-122">_alphaThresholdPercent \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="28f40-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-123">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="28f40-123">Type: **double**</span></span>

<span data-ttu-id="28f40-124">Пороговое значение альфа-канала, используемое для преобразования.</span><span class="sxs-lookup"><span data-stu-id="28f40-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="28f40-125">*палеттетранслате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28f40-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f40-126">Тип: **[ **викбитмаппалеттетипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="28f40-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="28f40-127">Тип перевода палитры, используемый для преобразования.</span><span class="sxs-lookup"><span data-stu-id="28f40-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f40-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28f40-128">Return value</span></span>

<span data-ttu-id="28f40-129">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="28f40-129">Type: **HRESULT**</span></span>

<span data-ttu-id="28f40-130">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="28f40-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28f40-131">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28f40-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28f40-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="28f40-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28f40-133">Требования</span><span class="sxs-lookup"><span data-stu-id="28f40-133">Requirements</span></span>



| <span data-ttu-id="28f40-134">Требование</span><span class="sxs-lookup"><span data-stu-id="28f40-134">Requirement</span></span> | <span data-ttu-id="28f40-135">Значение</span><span class="sxs-lookup"><span data-stu-id="28f40-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f40-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28f40-136">Minimum supported client</span></span><br/> | <span data-ttu-id="28f40-137">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28f40-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28f40-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28f40-138">Minimum supported server</span></span><br/> | <span data-ttu-id="28f40-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28f40-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28f40-140">DLL</span><span class="sxs-lookup"><span data-stu-id="28f40-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28f40-141"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28f40-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




