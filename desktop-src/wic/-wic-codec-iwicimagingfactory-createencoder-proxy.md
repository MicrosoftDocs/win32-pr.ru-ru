---
description: Функция-посредник для метода Креатинкодер.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: Функция IWICImagingFactory_CreateEncoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702394"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="202c7-103">IWICImagingFactory \_ креатинкодер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="202c7-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="202c7-104">Функция-посредник для метода [**креатинкодер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .</span><span class="sxs-lookup"><span data-stu-id="202c7-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="202c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="202c7-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="202c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="202c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202c7-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="202c7-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202c7-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="202c7-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="202c7-109">_guidContainerFormat \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="202c7-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202c7-110">Тип: **рефгуид**</span><span class="sxs-lookup"><span data-stu-id="202c7-110">Type: **REFGUID**</span></span>

<span data-ttu-id="202c7-111">Идентификатор GUID для требуемого формата контейнера.</span><span class="sxs-lookup"><span data-stu-id="202c7-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="202c7-112">*пгуидвендор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="202c7-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="202c7-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="202c7-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="202c7-114">Идентификатор GUID поставщика для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="202c7-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="202c7-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="202c7-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="202c7-116">Тип: **[ **ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="202c7-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="202c7-117">Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="202c7-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202c7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="202c7-118">Return value</span></span>

<span data-ttu-id="202c7-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="202c7-119">Type: **HRESULT**</span></span>

<span data-ttu-id="202c7-120">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="202c7-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="202c7-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="202c7-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="202c7-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="202c7-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="202c7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="202c7-123">Requirements</span></span>



| <span data-ttu-id="202c7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="202c7-124">Requirement</span></span> | <span data-ttu-id="202c7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="202c7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202c7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="202c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="202c7-127">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="202c7-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="202c7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="202c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="202c7-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="202c7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="202c7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="202c7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="202c7-131"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="202c7-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




