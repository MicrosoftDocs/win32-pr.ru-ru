---
description: Функция-посредник для метода Жетколорконтекстс.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: Функция IWICBitmapDecoder_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702402"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="16f91-103">Ивикбитмапдекодер \_ жетколорконтекстс \_ -функция</span><span class="sxs-lookup"><span data-stu-id="16f91-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="16f91-104">Функция-посредник для метода [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="16f91-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16f91-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="16f91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f91-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="16f91-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f91-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="16f91-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="16f91-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="16f91-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="16f91-110">*учетная запись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16f91-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f91-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="16f91-111">Type: **UINT**</span></span>

<span data-ttu-id="16f91-112">Число извлекаемых контекстных цветов.</span><span class="sxs-lookup"><span data-stu-id="16f91-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="16f91-113">Это значение должно быть размером или меньше, чем размер, доступный для *ппиколорконтекстс*.</span><span class="sxs-lookup"><span data-stu-id="16f91-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="16f91-114">*ппиколорконтекстс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="16f91-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16f91-115">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="16f91-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="16f91-116">Указатель, получающий указатель на [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="16f91-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="16f91-117">*пкактуалкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16f91-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16f91-118">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="16f91-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="16f91-119">Указатель, получающий количество цветовых контекстов, содержащихся в изображении.</span><span class="sxs-lookup"><span data-stu-id="16f91-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f91-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16f91-120">Return value</span></span>

<span data-ttu-id="16f91-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="16f91-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="16f91-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="16f91-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16f91-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16f91-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f91-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="16f91-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="16f91-125">Требования</span><span class="sxs-lookup"><span data-stu-id="16f91-125">Requirements</span></span>



| <span data-ttu-id="16f91-126">Требование</span><span class="sxs-lookup"><span data-stu-id="16f91-126">Requirement</span></span> | <span data-ttu-id="16f91-127">Значение</span><span class="sxs-lookup"><span data-stu-id="16f91-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f91-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16f91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="16f91-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16f91-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="16f91-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16f91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="16f91-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16f91-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="16f91-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16f91-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f91-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16f91-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




