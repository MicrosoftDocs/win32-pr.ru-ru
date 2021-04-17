---
description: Функция-посредник для метода Креатепалетте.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: Функция IWICImagingFactory_CreatePalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713057"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="e11aa-103">IWICImagingFactory \_ креатепалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e11aa-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="e11aa-104">Функция-посредник для метода [**креатепалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .</span><span class="sxs-lookup"><span data-stu-id="e11aa-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e11aa-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="e11aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e11aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11aa-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e11aa-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e11aa-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e11aa-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e11aa-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e11aa-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e11aa-110">Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="e11aa-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="e11aa-111">Указатель, получающий указатель на новый [**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span><span class="sxs-lookup"><span data-stu-id="e11aa-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11aa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e11aa-112">Return value</span></span>

<span data-ttu-id="e11aa-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e11aa-113">Type: **HRESULT**</span></span>

<span data-ttu-id="e11aa-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e11aa-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e11aa-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e11aa-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11aa-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="e11aa-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e11aa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e11aa-117">Requirements</span></span>



| <span data-ttu-id="e11aa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e11aa-118">Requirement</span></span> | <span data-ttu-id="e11aa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e11aa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11aa-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e11aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e11aa-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e11aa-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e11aa-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e11aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e11aa-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e11aa-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e11aa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e11aa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e11aa-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e11aa-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




