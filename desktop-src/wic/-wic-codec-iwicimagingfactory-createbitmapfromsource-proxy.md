---
description: Функция-посредник для метода Креатебитмапфромсаурце.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: Функция IWICImagingFactory_CreateBitmapFromSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999702"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="16496-103">IWICImagingFactory \_ креатебитмапфромсаурце \_ -функция</span><span class="sxs-lookup"><span data-stu-id="16496-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="16496-104">Функция-посредник для метода [**креатебитмапфромсаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .</span><span class="sxs-lookup"><span data-stu-id="16496-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16496-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16496-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="16496-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16496-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16496-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16496-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16496-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="16496-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="16496-109">_pIBitmapSource \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="16496-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16496-110">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="16496-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="16496-111">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) для создания точечного рисунка из.</span><span class="sxs-lookup"><span data-stu-id="16496-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="16496-112">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16496-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16496-113">Тип: **[ **викбитмапкреатекачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="16496-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="16496-114">Параметры кэша нового растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="16496-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="16496-115">*ппибитмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16496-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16496-116">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="16496-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="16496-117">Указатель, получающий указатель на новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="16496-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16496-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16496-118">Return value</span></span>

<span data-ttu-id="16496-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16496-119">Type: **HRESULT**</span></span>

<span data-ttu-id="16496-120">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="16496-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16496-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16496-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16496-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="16496-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="16496-123">Требования</span><span class="sxs-lookup"><span data-stu-id="16496-123">Requirements</span></span>



| <span data-ttu-id="16496-124">Требование</span><span class="sxs-lookup"><span data-stu-id="16496-124">Requirement</span></span> | <span data-ttu-id="16496-125">Значение</span><span class="sxs-lookup"><span data-stu-id="16496-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16496-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16496-126">Minimum supported client</span></span><br/> | <span data-ttu-id="16496-127">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16496-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="16496-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16496-128">Minimum supported server</span></span><br/> | <span data-ttu-id="16496-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16496-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="16496-130">DLL</span><span class="sxs-lookup"><span data-stu-id="16496-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16496-131"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16496-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




