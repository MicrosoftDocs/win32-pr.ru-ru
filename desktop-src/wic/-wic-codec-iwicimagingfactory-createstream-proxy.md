---
description: Функция-посредник для метода Креатестреам.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Функция IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702907"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="3de30-103">IWICImagingFactory \_ креатестреам \_ -функция</span><span class="sxs-lookup"><span data-stu-id="3de30-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="3de30-104">Функция-посредник для метода [**креатестреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .</span><span class="sxs-lookup"><span data-stu-id="3de30-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3de30-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="3de30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3de30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de30-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3de30-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de30-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="3de30-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="3de30-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3de30-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3de30-110">Тип: **[ **ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="3de30-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="3de30-111">Указатель, получающий указатель на новый [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span><span class="sxs-lookup"><span data-stu-id="3de30-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de30-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3de30-112">Return value</span></span>

<span data-ttu-id="3de30-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3de30-113">Type: **HRESULT**</span></span>

<span data-ttu-id="3de30-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3de30-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3de30-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3de30-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de30-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="3de30-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3de30-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3de30-117">Requirements</span></span>



| <span data-ttu-id="3de30-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3de30-118">Requirement</span></span> | <span data-ttu-id="3de30-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3de30-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de30-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3de30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3de30-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3de30-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3de30-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3de30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3de30-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3de30-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3de30-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3de30-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3de30-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3de30-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




