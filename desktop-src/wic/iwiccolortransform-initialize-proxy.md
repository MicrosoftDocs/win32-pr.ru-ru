---
description: Инициализирует Ивикколортрансформ с IWICBitmapSource и преобразует его из одного Ивикколорконтекст в другой.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Функция IWICColorTransform_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704368"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="de2c1-103">Ивикколортрансформ \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="de2c1-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="de2c1-104">Инициализирует [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) с [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) и преобразует его из одного [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) в другой.</span><span class="sxs-lookup"><span data-stu-id="de2c1-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de2c1-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="de2c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de2c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de2c1-107">*пиколортрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de2c1-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2c1-108">Тип: **[ **ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="de2c1-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="de2c1-109">Преобразование цвета для инициализации.</span><span class="sxs-lookup"><span data-stu-id="de2c1-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="de2c1-110">*пибитмапсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de2c1-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2c1-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="de2c1-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="de2c1-112">Источник растрового изображения, используемый для инициализации преобразования цвета.</span><span class="sxs-lookup"><span data-stu-id="de2c1-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="de2c1-113">*пиконтекстсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de2c1-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2c1-114">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="de2c1-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="de2c1-115">Источник цветового контекста.</span><span class="sxs-lookup"><span data-stu-id="de2c1-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="de2c1-116">*пиконтекстдест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de2c1-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2c1-117">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="de2c1-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="de2c1-118">Назначение контекста цвета.</span><span class="sxs-lookup"><span data-stu-id="de2c1-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="de2c1-119">*пикселфмтдест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de2c1-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2c1-120">Тип: **рефвикпикселформатгуид**</span><span class="sxs-lookup"><span data-stu-id="de2c1-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="de2c1-121">Идентификатор GUID требуемого формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="de2c1-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de2c1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de2c1-122">Return value</span></span>

<span data-ttu-id="de2c1-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de2c1-123">Type: **HRESULT**</span></span>

<span data-ttu-id="de2c1-124">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="de2c1-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de2c1-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de2c1-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de2c1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="de2c1-126">Requirements</span></span>



| <span data-ttu-id="de2c1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="de2c1-127">Requirement</span></span> | <span data-ttu-id="de2c1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="de2c1-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2c1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="de2c1-129">DLL</span></span><br/> | <dl> <span data-ttu-id="de2c1-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de2c1-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




