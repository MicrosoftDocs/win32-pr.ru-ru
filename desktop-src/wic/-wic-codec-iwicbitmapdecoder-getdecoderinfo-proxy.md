---
description: Функция-посредник для метода Жетдекодеринфо.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: Функция IWICBitmapDecoder_GetDecoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497331"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="b5ee4-103">Ивикбитмапдекодер \_ жетдекодеринфо \_ -функция</span><span class="sxs-lookup"><span data-stu-id="b5ee4-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="b5ee4-104">Функция-посредник для метода [**жетдекодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="b5ee4-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ee4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5ee4-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b5ee4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ee4-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="b5ee4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ee4-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b5ee4-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b5ee4-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="b5ee4-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b5ee4-110">*ппидекодеринфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5ee4-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ee4-111">Тип: **[ **ивикбитмапдекодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="b5ee4-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="b5ee4-112">Указатель, получающий указатель на [**ивикбитмапдекодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span><span class="sxs-lookup"><span data-stu-id="b5ee4-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ee4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5ee4-113">Return value</span></span>

<span data-ttu-id="b5ee4-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5ee4-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b5ee4-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b5ee4-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5ee4-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5ee4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ee4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="b5ee4-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ee4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ee4-118">Requirements</span></span>



| <span data-ttu-id="b5ee4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ee4-119">Requirement</span></span> | <span data-ttu-id="b5ee4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ee4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ee4-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5ee4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ee4-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5ee4-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b5ee4-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5ee4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ee4-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5ee4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b5ee4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ee4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ee4-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5ee4-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




