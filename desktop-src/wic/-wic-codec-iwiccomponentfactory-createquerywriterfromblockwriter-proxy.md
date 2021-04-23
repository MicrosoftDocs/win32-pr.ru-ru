---
description: Функция-посредник для метода Креатекуеривритерфромблокквритер.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: Функция IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265866"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="51210-103">Ивиккомпонентфактори \_ креатекуеривритерфромблокквритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="51210-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="51210-104">Функция-посредник для метода [**креатекуеривритерфромблокквритер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .</span><span class="sxs-lookup"><span data-stu-id="51210-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51210-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51210-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="51210-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51210-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="51210-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51210-108">Тип: \**[**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="51210-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="51210-109">Указатель на этот объект [_ *ивиккомпонентфактори* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="51210-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="51210-110">*пиблокквритер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51210-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51210-111">Тип: \**[**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="51210-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="51210-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="51210-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51210-113">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="51210-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51210-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51210-114">Return value</span></span>

<span data-ttu-id="51210-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="51210-115">Type: **HRESULT**</span></span>

<span data-ttu-id="51210-116">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="51210-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51210-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51210-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51210-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="51210-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="51210-119">Требования</span><span class="sxs-lookup"><span data-stu-id="51210-119">Requirements</span></span>



| <span data-ttu-id="51210-120">Требование</span><span class="sxs-lookup"><span data-stu-id="51210-120">Requirement</span></span> | <span data-ttu-id="51210-121">Значение</span><span class="sxs-lookup"><span data-stu-id="51210-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51210-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51210-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51210-123">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51210-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="51210-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51210-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51210-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51210-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="51210-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51210-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51210-127"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51210-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




