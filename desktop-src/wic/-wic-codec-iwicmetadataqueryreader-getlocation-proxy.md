---
description: Функция-посредник для метода методического расположения.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: Функция IWICMetadataQueryReader_GetLocation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674389"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="dd8f2-103">\_ \_ Функция прокси Ивикметадатакуериреадер-размещения</span><span class="sxs-lookup"><span data-stu-id="dd8f2-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="dd8f2-104">Функция-посредник для метода методического [**расположения**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .</span><span class="sxs-lookup"><span data-stu-id="dd8f2-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd8f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd8f2-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="dd8f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd8f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd8f2-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8f2-108">Тип: \**[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="dd8f2-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="dd8f2-109">Указатель на этот объект [_ *ивикметадатакуериреадер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="dd8f2-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="dd8f2-110">*кчмаксленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8f2-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="dd8f2-111">Type: **UINT**</span></span>

<span data-ttu-id="dd8f2-112">Длина буфера *взнамеспаце* .</span><span class="sxs-lookup"><span data-stu-id="dd8f2-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dd8f2-113">*взнамеспаце* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8f2-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="dd8f2-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="dd8f2-115">Указатель, получающий текущее расположение пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dd8f2-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="dd8f2-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8f2-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="dd8f2-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="dd8f2-118">Фактическая длина буфера, необходимая для получения текущего расположения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dd8f2-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd8f2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd8f2-119">Return value</span></span>

<span data-ttu-id="dd8f2-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dd8f2-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dd8f2-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dd8f2-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd8f2-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd8f2-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8f2-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="dd8f2-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dd8f2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="dd8f2-124">Requirements</span></span>



| <span data-ttu-id="dd8f2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="dd8f2-125">Requirement</span></span> | <span data-ttu-id="dd8f2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8f2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8f2-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd8f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dd8f2-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dd8f2-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd8f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dd8f2-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd8f2-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dd8f2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dd8f2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd8f2-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd8f2-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




