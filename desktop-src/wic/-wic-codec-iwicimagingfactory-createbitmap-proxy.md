---
description: Функция-посредник для метода Креатебитмап.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: Функция IWICImagingFactory_CreateBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712619"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="73aaa-103">IWICImagingFactory \_ креатебитмап \_ -функция</span><span class="sxs-lookup"><span data-stu-id="73aaa-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="73aaa-104">Функция-посредник для метода [**креатебитмап**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .</span><span class="sxs-lookup"><span data-stu-id="73aaa-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73aaa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73aaa-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="73aaa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73aaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73aaa-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="73aaa-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="73aaa-109">_uiWidth \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="73aaa-110">Type: **UINT**</span></span>

<span data-ttu-id="73aaa-111">Ширина нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="73aaa-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="73aaa-112">*уихеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="73aaa-113">Type: **UINT**</span></span>

<span data-ttu-id="73aaa-114">Высота нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="73aaa-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="73aaa-115">*PixelFormat* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-116">Тип: **рефвикпикселформатгуид**</span><span class="sxs-lookup"><span data-stu-id="73aaa-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="73aaa-117">Формат пикселей нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="73aaa-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="73aaa-118">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-119">Тип: **[ **викбитмапкреатекачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="73aaa-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="73aaa-120">Параметры создания кэша нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="73aaa-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="73aaa-121">*ппибитмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73aaa-122">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="73aaa-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="73aaa-123">Указатель, получающий указатель на новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="73aaa-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73aaa-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73aaa-124">Return value</span></span>

<span data-ttu-id="73aaa-125">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73aaa-125">Type: **HRESULT**</span></span>

<span data-ttu-id="73aaa-126">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="73aaa-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73aaa-127">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73aaa-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73aaa-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="73aaa-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="73aaa-129">Требования</span><span class="sxs-lookup"><span data-stu-id="73aaa-129">Requirements</span></span>



| <span data-ttu-id="73aaa-130">Требование</span><span class="sxs-lookup"><span data-stu-id="73aaa-130">Requirement</span></span> | <span data-ttu-id="73aaa-131">Значение</span><span class="sxs-lookup"><span data-stu-id="73aaa-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73aaa-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73aaa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="73aaa-133">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="73aaa-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73aaa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="73aaa-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73aaa-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="73aaa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="73aaa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73aaa-137"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73aaa-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




