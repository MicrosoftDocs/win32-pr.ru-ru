---
description: IWICBitmapSource_CopyPalette_Proxy функция-прокси для метода Копипалетте.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Функция IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100502"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="5e0ae-103">IWICBitmapSource \_ копипалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="5e0ae-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="5e0ae-104">Функция-посредник для метода [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="5e0ae-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e0ae-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="5e0ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e0ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0ae-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="5e0ae-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0ae-108">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="5e0ae-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="5e0ae-109">Указатель на этот объект [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="5e0ae-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="5e0ae-110">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e0ae-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0ae-111">Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="5e0ae-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="5e0ae-112">Палитра.</span><span class="sxs-lookup"><span data-stu-id="5e0ae-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0ae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e0ae-113">Return value</span></span>

<span data-ttu-id="5e0ae-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e0ae-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5e0ae-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e0ae-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e0ae-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e0ae-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e0ae-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="5e0ae-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0ae-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5e0ae-118">Requirements</span></span>



| <span data-ttu-id="5e0ae-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5e0ae-119">Requirement</span></span> | <span data-ttu-id="5e0ae-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5e0ae-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0ae-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e0ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0ae-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e0ae-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5e0ae-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e0ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0ae-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e0ae-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5e0ae-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5e0ae-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e0ae-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e0ae-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




