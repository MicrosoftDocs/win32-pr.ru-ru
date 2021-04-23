---
description: Функция-посредник для метода Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: Функция IWICBitmapScaler_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703326"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="cd6d0-103">Ивикбитмапскалер \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="cd6d0-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="cd6d0-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="cd6d0-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd6d0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="cd6d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd6d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6d0-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d0-108">Тип: \**[**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="cd6d0-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="cd6d0-109">Указатель на этот объект [_ *ивикбитмапскалер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="cd6d0-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d0-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d0-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="cd6d0-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="cd6d0-112">Источник входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="cd6d0-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d0-113">_uiWidth \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d0-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="cd6d0-114">Type: **UINT**</span></span>

<span data-ttu-id="cd6d0-115">Целевая ширина.</span><span class="sxs-lookup"><span data-stu-id="cd6d0-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d0-116">*уихеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d0-117">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="cd6d0-117">Type: **UINT**</span></span>

<span data-ttu-id="cd6d0-118">Высота конечный.</span><span class="sxs-lookup"><span data-stu-id="cd6d0-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d0-119">*режим* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d0-120">Тип: **[ **викбитмапинтерполатионмоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="cd6d0-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="cd6d0-121">Режим интерполяции, используемый при масштабировании.</span><span class="sxs-lookup"><span data-stu-id="cd6d0-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6d0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd6d0-122">Return value</span></span>

<span data-ttu-id="cd6d0-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd6d0-123">Type: **HRESULT**</span></span>

<span data-ttu-id="cd6d0-124">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd6d0-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd6d0-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd6d0-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd6d0-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="cd6d0-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6d0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cd6d0-127">Requirements</span></span>



| <span data-ttu-id="cd6d0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cd6d0-128">Requirement</span></span> | <span data-ttu-id="cd6d0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6d0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6d0-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd6d0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6d0-131">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cd6d0-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd6d0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6d0-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd6d0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cd6d0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cd6d0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd6d0-135"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd6d0-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




