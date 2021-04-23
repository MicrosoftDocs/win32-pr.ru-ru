---
description: Функция-посредник для метода "методом".
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: Функция IWICBitmapSource_GetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264873"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="6f66d-103">\_ \_ Функция прокси-сервера IWICBitmapSource с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="6f66d-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="6f66d-104">Функция-посредник для [**метода "**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) методом".</span><span class="sxs-lookup"><span data-stu-id="6f66d-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f66d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f66d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="6f66d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f66d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f66d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f66d-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="6f66d-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="6f66d-109">Указатель на этот объект [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="6f66d-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="6f66d-110">*пдпикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f66d-111">Тип: \**Двойное \** _</span><span class="sxs-lookup"><span data-stu-id="6f66d-111">Type: \**double\** _</span></span>

<span data-ttu-id="6f66d-112">Указатель, получающий разрешение dpi по оси x.</span><span class="sxs-lookup"><span data-stu-id="6f66d-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="6f66d-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f66d-114">Тип: \**Двойное \** _</span><span class="sxs-lookup"><span data-stu-id="6f66d-114">Type: \**double\** _</span></span>

<span data-ttu-id="6f66d-115">Указатель, получающий разрешение dpi по оси y.</span><span class="sxs-lookup"><span data-stu-id="6f66d-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f66d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f66d-116">Return value</span></span>

<span data-ttu-id="6f66d-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6f66d-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6f66d-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6f66d-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f66d-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f66d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f66d-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="6f66d-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6f66d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6f66d-121">Requirements</span></span>



| <span data-ttu-id="6f66d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6f66d-122">Requirement</span></span> | <span data-ttu-id="6f66d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6f66d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f66d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f66d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f66d-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6f66d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f66d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f66d-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6f66d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6f66d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f66d-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f66d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




