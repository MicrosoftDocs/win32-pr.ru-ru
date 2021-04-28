---
description: IWICBitmapScaler_Initialize_Proxy функция-прокси для метода Initialize.
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
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100542"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="5ee1c-103">Ивикбитмапскалер \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="5ee1c-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="5ee1c-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="5ee1c-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ee1c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="5ee1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ee1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee1c-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee1c-108">Тип: **[ **ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span><span class="sxs-lookup"><span data-stu-id="5ee1c-108">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span></span>

<span data-ttu-id="5ee1c-109">Указатель на этот объект [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="5ee1c-109">Pointer to this [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="5ee1c-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee1c-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="5ee1c-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="5ee1c-112">Источник входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="5ee1c-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="5ee1c-113">*уивидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-113">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee1c-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="5ee1c-114">Type: **UINT**</span></span>

<span data-ttu-id="5ee1c-115">Целевая ширина.</span><span class="sxs-lookup"><span data-stu-id="5ee1c-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="5ee1c-116">*уихеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee1c-117">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="5ee1c-117">Type: **UINT**</span></span>

<span data-ttu-id="5ee1c-118">Высота конечный.</span><span class="sxs-lookup"><span data-stu-id="5ee1c-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="5ee1c-119">*режим* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee1c-120">Тип: **[ **викбитмапинтерполатионмоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="5ee1c-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="5ee1c-121">Режим интерполяции, используемый при масштабировании.</span><span class="sxs-lookup"><span data-stu-id="5ee1c-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee1c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ee1c-122">Return value</span></span>

<span data-ttu-id="5ee1c-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5ee1c-123">Type: **HRESULT**</span></span>

<span data-ttu-id="5ee1c-124">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5ee1c-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ee1c-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ee1c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee1c-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="5ee1c-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee1c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5ee1c-127">Requirements</span></span>



| <span data-ttu-id="5ee1c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5ee1c-128">Requirement</span></span> | <span data-ttu-id="5ee1c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5ee1c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee1c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ee1c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee1c-131">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5ee1c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ee1c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee1c-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ee1c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5ee1c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5ee1c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ee1c-135"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ee1c-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




