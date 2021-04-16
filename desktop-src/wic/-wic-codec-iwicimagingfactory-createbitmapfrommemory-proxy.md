---
description: Функция-посредник для метода Креатебитмапфроммемори.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Функция IWICImagingFactory_CreateBitmapFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664293"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="e75ad-103">IWICImagingFactory \_ креатебитмапфроммемори \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e75ad-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="e75ad-104">Функция-посредник для метода [**креатебитмапфроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .</span><span class="sxs-lookup"><span data-stu-id="e75ad-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e75ad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e75ad-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="e75ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e75ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75ad-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e75ad-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-109">_uiWidth \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e75ad-110">Type: **UINT**</span></span>

<span data-ttu-id="e75ad-111">Ширина нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="e75ad-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-112">*уихеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e75ad-113">Type: **UINT**</span></span>

<span data-ttu-id="e75ad-114">Высота нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="e75ad-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-115">*PixelFormat* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-116">Тип: **рефвикпикселформатгуид**</span><span class="sxs-lookup"><span data-stu-id="e75ad-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="e75ad-117">Формат пикселей нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="e75ad-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-118">*кбстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e75ad-119">Type: **UINT**</span></span>

<span data-ttu-id="e75ad-120">[*Шаг*](/windows) с заданными данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="e75ad-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-121">*кббуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-122">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e75ad-122">Type: **UINT**</span></span>

<span data-ttu-id="e75ad-123">Размер *пббуффер*.</span><span class="sxs-lookup"><span data-stu-id="e75ad-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-124">*пббуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-125">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="e75ad-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="e75ad-126">Буфер, используемый для создания точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="e75ad-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e75ad-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ad-128">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="e75ad-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="e75ad-129">Указатель, получающий указатель на новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="e75ad-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75ad-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e75ad-130">Return value</span></span>

<span data-ttu-id="e75ad-131">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e75ad-131">Type: **HRESULT**</span></span>

<span data-ttu-id="e75ad-132">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e75ad-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e75ad-133">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e75ad-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75ad-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="e75ad-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e75ad-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e75ad-135">Requirements</span></span>



| <span data-ttu-id="e75ad-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e75ad-136">Requirement</span></span> | <span data-ttu-id="e75ad-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e75ad-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75ad-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e75ad-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e75ad-139">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e75ad-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e75ad-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e75ad-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e75ad-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e75ad-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e75ad-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e75ad-143"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e75ad-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

