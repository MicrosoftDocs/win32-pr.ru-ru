---
description: Функция-посредник для метода Креатебитмапфлипротатор.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: Функция IWICImagingFactory_CreateBitmapFlipRotator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664294"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="f64f6-103">IWICImagingFactory \_ креатебитмапфлипротатор \_ -функция</span><span class="sxs-lookup"><span data-stu-id="f64f6-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="f64f6-104">Функция-посредник для метода [**креатебитмапфлипротатор**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="f64f6-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f64f6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="f64f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f64f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64f6-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f64f6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f64f6-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f64f6-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f64f6-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f64f6-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f64f6-110">Тип: **[ **ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="f64f6-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="f64f6-111">Указатель, получающий указатель на новый [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span><span class="sxs-lookup"><span data-stu-id="f64f6-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f64f6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f64f6-112">Return value</span></span>

<span data-ttu-id="f64f6-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f64f6-113">Type: **HRESULT**</span></span>

<span data-ttu-id="f64f6-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f64f6-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f64f6-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f64f6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f64f6-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f64f6-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f64f6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f64f6-117">Requirements</span></span>



| <span data-ttu-id="f64f6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f64f6-118">Requirement</span></span> | <span data-ttu-id="f64f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f64f6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64f6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f64f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f64f6-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f64f6-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f64f6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f64f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f64f6-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f64f6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f64f6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f64f6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f64f6-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f64f6-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




