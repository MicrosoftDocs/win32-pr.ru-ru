---
description: Функция-посредник для метода Креатекуеривритер.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: Функция IWICImagingFactory_CreateQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817105"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="47dc2-103">IWICImagingFactory \_ креатекуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="47dc2-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="47dc2-104">Функция-посредник для метода [**креатекуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="47dc2-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47dc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47dc2-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="47dc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47dc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47dc2-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47dc2-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="47dc2-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="47dc2-109">_guidMetadataFormat \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47dc2-110">Тип: **рефгуид**</span><span class="sxs-lookup"><span data-stu-id="47dc2-110">Type: **REFGUID**</span></span>

<span data-ttu-id="47dc2-111">Идентификатор GUID для требуемого формата метаданных.</span><span class="sxs-lookup"><span data-stu-id="47dc2-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="47dc2-112">*пгуидвендор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47dc2-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="47dc2-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="47dc2-114">Идентификатор GUID поставщика модуля записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="47dc2-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="47dc2-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47dc2-116">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="47dc2-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="47dc2-117">Указатель, получающий указатель на новый [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="47dc2-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47dc2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47dc2-118">Return value</span></span>

<span data-ttu-id="47dc2-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="47dc2-119">Type: **HRESULT**</span></span>

<span data-ttu-id="47dc2-120">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="47dc2-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="47dc2-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="47dc2-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="47dc2-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="47dc2-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="47dc2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="47dc2-123">Requirements</span></span>



| <span data-ttu-id="47dc2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="47dc2-124">Requirement</span></span> | <span data-ttu-id="47dc2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="47dc2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47dc2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47dc2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47dc2-127">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="47dc2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47dc2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47dc2-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47dc2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="47dc2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="47dc2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47dc2-131"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47dc2-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




