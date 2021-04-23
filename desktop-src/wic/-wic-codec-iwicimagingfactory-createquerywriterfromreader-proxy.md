---
description: Функция-посредник для метода Креатекуеривритерфромреадер.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: Функция IWICImagingFactory_CreateQueryWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999342"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="cd16a-103">IWICImagingFactory \_ креатекуеривритерфромреадер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="cd16a-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="cd16a-104">Функция-посредник для метода [**креатекуеривритерфромреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="cd16a-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd16a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd16a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="cd16a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd16a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd16a-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd16a-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cd16a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cd16a-109">_pIQueryReader \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd16a-110">Тип: \**[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="cd16a-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="cd16a-111">Средство чтения запросов метаданных, из которого создается модуль записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="cd16a-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="cd16a-112">_pguidVendor \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd16a-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="cd16a-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="cd16a-114">Идентификатор GUID поставщика для модуля записи запросов метаданных.</span><span class="sxs-lookup"><span data-stu-id="cd16a-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="cd16a-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd16a-116">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="cd16a-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="cd16a-117">Указатель, получающий указатель на новый [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="cd16a-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd16a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd16a-118">Return value</span></span>

<span data-ttu-id="cd16a-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd16a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="cd16a-120">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd16a-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd16a-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd16a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd16a-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="cd16a-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cd16a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cd16a-123">Requirements</span></span>



| <span data-ttu-id="cd16a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cd16a-124">Requirement</span></span> | <span data-ttu-id="cd16a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cd16a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd16a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd16a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd16a-127">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cd16a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd16a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd16a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd16a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cd16a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cd16a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd16a-131"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd16a-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




