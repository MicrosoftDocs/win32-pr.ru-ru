---
description: Функция-посредник для метода NOFRAMES.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: Функция IWICBitmapDecoder_GetFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343225"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="89325-103">\_ \_ Функция прокси-сервера ивикбитмапдекодер NOFRAMES</span><span class="sxs-lookup"><span data-stu-id="89325-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="89325-104">Функция-посредник для метода [**noframes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .</span><span class="sxs-lookup"><span data-stu-id="89325-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89325-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89325-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="89325-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89325-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="89325-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89325-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="89325-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="89325-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="89325-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="89325-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89325-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89325-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="89325-111">Type: **UINT**</span></span>

<span data-ttu-id="89325-112">Определенный кадр для извлечения.</span><span class="sxs-lookup"><span data-stu-id="89325-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="89325-113">*ппибитмапфраме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="89325-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89325-114">Тип: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="89325-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="89325-115">Указатель, получающий указатель на [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="89325-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89325-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89325-116">Return value</span></span>

<span data-ttu-id="89325-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89325-117">Type: **HRESULT**</span></span>

<span data-ttu-id="89325-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="89325-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89325-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89325-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89325-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="89325-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="89325-121">Требования</span><span class="sxs-lookup"><span data-stu-id="89325-121">Requirements</span></span>



| <span data-ttu-id="89325-122">Требование</span><span class="sxs-lookup"><span data-stu-id="89325-122">Requirement</span></span> | <span data-ttu-id="89325-123">Значение</span><span class="sxs-lookup"><span data-stu-id="89325-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89325-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89325-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89325-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89325-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="89325-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89325-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89325-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89325-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="89325-128">DLL</span><span class="sxs-lookup"><span data-stu-id="89325-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89325-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89325-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




