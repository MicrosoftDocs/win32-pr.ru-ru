---
description: Функция-посредник для метода Жетконтаинерформат.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Функция IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702321"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="2e4f0-103">Ивикметадатакуериреадер \_ жетконтаинерформат \_ -функция</span><span class="sxs-lookup"><span data-stu-id="2e4f0-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="2e4f0-104">Функция-посредник для метода [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="2e4f0-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e4f0-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2e4f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e4f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4f0-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="2e4f0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4f0-108">Тип: \**[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="2e4f0-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="2e4f0-109">Указатель на этот объект [_ *ивикметадатакуериреадер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="2e4f0-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e4f0-110">*пгуидконтаинерформат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2e4f0-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4f0-111">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="2e4f0-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="2e4f0-112">Указатель, который получает идентификатор GUID формата коинтаинер.</span><span class="sxs-lookup"><span data-stu-id="2e4f0-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4f0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e4f0-113">Return value</span></span>

<span data-ttu-id="2e4f0-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2e4f0-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2e4f0-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2e4f0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e4f0-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e4f0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e4f0-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="2e4f0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4f0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e4f0-118">Requirements</span></span>



| <span data-ttu-id="2e4f0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e4f0-119">Requirement</span></span> | <span data-ttu-id="2e4f0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e4f0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4f0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e4f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4f0-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e4f0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e4f0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e4f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4f0-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e4f0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e4f0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e4f0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4f0-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e4f0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




