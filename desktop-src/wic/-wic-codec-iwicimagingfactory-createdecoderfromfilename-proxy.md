---
description: Функция-посредник для метода Креатедекодерфромфиленаме.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: Функция IWICImagingFactory_CreateDecoderFromFilename_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693718"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="38bc6-103">IWICImagingFactory \_ креатедекодерфромфиленаме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="38bc6-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="38bc6-104">Функция-посредник для метода [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="38bc6-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38bc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38bc6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="38bc6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38bc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38bc6-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-108">Тип: \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="38bc6-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-109">_wzFilename \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-110">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="38bc6-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="38bc6-111">Указатель на строку, завершающуюся нулем, которая указывает имя объекта для создания или открытия.</span><span class="sxs-lookup"><span data-stu-id="38bc6-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-112">*пгуидвендор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="38bc6-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="38bc6-114">Идентификатор GUID поставщика для декодера.</span><span class="sxs-lookup"><span data-stu-id="38bc6-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-115">_dwDesiredAccess \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-116">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="38bc6-116">Type: **DWORD**</span></span>

<span data-ttu-id="38bc6-117">Доступ к объекту, который может быть доступен для чтения, записи или для того и другого.</span><span class="sxs-lookup"><span data-stu-id="38bc6-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="38bc6-118">Дополнительные сведения см. в разделе File [Security and Access \[ Rights \] Files](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="38bc6-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-119">*метадатаоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-120">Тип: **[ **викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="38bc6-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="38bc6-121">[**Викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , используемый при создании декодера.</span><span class="sxs-lookup"><span data-stu-id="38bc6-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-122">*ппидекодер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-123">Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="38bc6-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="38bc6-124">Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="38bc6-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38bc6-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38bc6-125">Return value</span></span>

<span data-ttu-id="38bc6-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="38bc6-126">Type: **HRESULT**</span></span>

<span data-ttu-id="38bc6-127">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="38bc6-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38bc6-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38bc6-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38bc6-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="38bc6-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="38bc6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="38bc6-130">Requirements</span></span>



| <span data-ttu-id="38bc6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="38bc6-131">Requirement</span></span> | <span data-ttu-id="38bc6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="38bc6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38bc6-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38bc6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38bc6-134">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="38bc6-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38bc6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38bc6-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="38bc6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="38bc6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38bc6-138"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38bc6-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

