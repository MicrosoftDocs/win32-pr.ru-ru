---
description: Функция-посредник для метода Креатекомпонентинфо.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: Функция IWICImagingFactory_CreateComponentInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347862"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="a08d3-103">IWICImagingFactory \_ креатекомпонентинфо \_ -функция</span><span class="sxs-lookup"><span data-stu-id="a08d3-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="a08d3-104">Функция-посредник для метода [**креатекомпонентинфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="a08d3-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a08d3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a08d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a08d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08d3-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a08d3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d3-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a08d3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a08d3-109">_clsidComponent \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a08d3-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d3-110">Тип: **рефклсид**</span><span class="sxs-lookup"><span data-stu-id="a08d3-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="a08d3-111">Идентификатор CLSID для требуемого компонента.</span><span class="sxs-lookup"><span data-stu-id="a08d3-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="a08d3-112">*ппиинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a08d3-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d3-113">Тип: **[ **ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="a08d3-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="a08d3-114">Указатель, получающий указатель на новый [**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span><span class="sxs-lookup"><span data-stu-id="a08d3-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08d3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a08d3-115">Return value</span></span>

<span data-ttu-id="a08d3-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a08d3-116">Type: **HRESULT**</span></span>

<span data-ttu-id="a08d3-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a08d3-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a08d3-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a08d3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08d3-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="a08d3-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a08d3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a08d3-120">Requirements</span></span>



| <span data-ttu-id="a08d3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a08d3-121">Requirement</span></span> | <span data-ttu-id="a08d3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a08d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08d3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a08d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a08d3-124">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a08d3-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a08d3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a08d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a08d3-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a08d3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a08d3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a08d3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08d3-128"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a08d3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




