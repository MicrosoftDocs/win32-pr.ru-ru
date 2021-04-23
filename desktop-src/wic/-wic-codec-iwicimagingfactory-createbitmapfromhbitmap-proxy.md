---
description: Функция-посредник для метода Креатебитмапфромхбитмап.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: Функция IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684204"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="f3bb3-103">IWICImagingFactory \_ креатебитмапфромхбитмап \_ -функция</span><span class="sxs-lookup"><span data-stu-id="f3bb3-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="f3bb3-104">Функция-посредник для метода [**креатебитмапфромхбитмап**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .</span><span class="sxs-lookup"><span data-stu-id="f3bb3-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3bb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3bb3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="f3bb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3bb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3bb3-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bb3-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f3bb3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f3bb3-109">_hBitmap \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bb3-110">Тип: **хбитмап**</span><span class="sxs-lookup"><span data-stu-id="f3bb3-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="f3bb3-111">Маркер точечного рисунка для создания точечного рисунка из.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="f3bb3-112">*хпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bb3-113">Тип: **хпалетте**</span><span class="sxs-lookup"><span data-stu-id="f3bb3-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="f3bb3-114">Маркер палитры, используемый для создания точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f3bb3-115">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bb3-116">Тип: **[ **викбитмапалфачаннелоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="f3bb3-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="f3bb3-117">Параметры альфа-канала для создания точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f3bb3-118">*ппибитмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bb3-119">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="f3bb3-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="f3bb3-120">Указатель, получающий указатель на новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3bb3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3bb3-121">Return value</span></span>

<span data-ttu-id="f3bb3-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f3bb3-122">Type: **HRESULT**</span></span>

<span data-ttu-id="f3bb3-123">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3bb3-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3bb3-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3bb3-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="f3bb3-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3bb3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f3bb3-126">Requirements</span></span>



| <span data-ttu-id="f3bb3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f3bb3-127">Requirement</span></span> | <span data-ttu-id="f3bb3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f3bb3-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3bb3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3bb3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bb3-130">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f3bb3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3bb3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bb3-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3bb3-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f3bb3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f3bb3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3bb3-134"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3bb3-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




