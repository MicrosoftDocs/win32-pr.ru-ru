---
description: Функция-посредник для метода Жетчаннелмаск.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: Функция IWICPixelFormatInfo_GetChannelMask_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272303"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="938d1-103">Ивикпикселформатинфо \_ жетчаннелмаск \_ -функция</span><span class="sxs-lookup"><span data-stu-id="938d1-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="938d1-104">Функция-посредник для метода [**жетчаннелмаск**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .</span><span class="sxs-lookup"><span data-stu-id="938d1-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="938d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="938d1-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="938d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="938d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="938d1-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="938d1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d1-108">Тип: \**[**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="938d1-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="938d1-109">Указатель на этот объект [_ *ивикпикселформатинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="938d1-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="938d1-110">*уичаннелиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="938d1-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d1-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="938d1-111">Type: **UINT**</span></span>

<span data-ttu-id="938d1-112">Индекс для извлекаемой маски канала.</span><span class="sxs-lookup"><span data-stu-id="938d1-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="938d1-113">*кбмаскбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="938d1-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d1-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="938d1-114">Type: **UINT**</span></span>

<span data-ttu-id="938d1-115">Размер буфера *пбмаскбуффер* .</span><span class="sxs-lookup"><span data-stu-id="938d1-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="938d1-116">*пбмаскбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="938d1-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="938d1-117">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="938d1-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="938d1-118">Указатель на буфер маски.</span><span class="sxs-lookup"><span data-stu-id="938d1-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="938d1-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="938d1-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="938d1-120">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="938d1-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="938d1-121">Фактический размер буфера, необходимый для получения маски канала.</span><span class="sxs-lookup"><span data-stu-id="938d1-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="938d1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="938d1-122">Return value</span></span>

<span data-ttu-id="938d1-123">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="938d1-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="938d1-124">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="938d1-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="938d1-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="938d1-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="938d1-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="938d1-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="938d1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="938d1-127">Requirements</span></span>



| <span data-ttu-id="938d1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="938d1-128">Requirement</span></span> | <span data-ttu-id="938d1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="938d1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="938d1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="938d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="938d1-131">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="938d1-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="938d1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="938d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="938d1-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="938d1-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="938d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="938d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="938d1-135"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="938d1-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




