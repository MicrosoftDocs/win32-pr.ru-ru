---
description: Функция-посредник для метода Креатеметадатавритерфромреадер.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: Функция IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910420"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="7f8e7-103">Ивиккомпонентфактори \_ креатеметадатавритерфромреадер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="7f8e7-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="7f8e7-104">Функция-посредник для метода [**креатеметадатавритерфромреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="7f8e7-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f8e7-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="7f8e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f8e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8e7-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8e7-108">Тип: \**[**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="7f8e7-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="7f8e7-109">Указатель на этот объект [_ *ивиккомпонентфактори* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="7f8e7-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="7f8e7-110">*пиреадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8e7-111">Тип: \**[**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="7f8e7-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="7f8e7-112">_pguidVendor \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8e7-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="7f8e7-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="7f8e7-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8e7-115">Тип: **[ **ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="7f8e7-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8e7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f8e7-116">Return value</span></span>

<span data-ttu-id="7f8e7-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-117">Type: **HRESULT**</span></span>

<span data-ttu-id="7f8e7-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f8e7-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f8e7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8e7-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="7f8e7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8e7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7f8e7-121">Requirements</span></span>



| <span data-ttu-id="7f8e7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7f8e7-122">Requirement</span></span> | <span data-ttu-id="7f8e7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7f8e7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8e7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f8e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8e7-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7f8e7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f8e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8e7-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7f8e7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7f8e7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f8e7-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f8e7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




