---
description: IWICBitmapDecoder_GetColorContexts_Proxy функция-прокси для метода Жетколорконтекстс.
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
ms.openlocfilehash: e550ca4ebd863e58a4bd285c48a2a01aad059b03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086262"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="de133-103">Ивикбитмапдекодер \_ жетколорконтекстс \_ -функция</span><span class="sxs-lookup"><span data-stu-id="de133-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="de133-104">Функция-посредник для метода [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="de133-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de133-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de133-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="de133-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de133-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="de133-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de133-108">Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="de133-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="de133-109">Указатель на этот объект [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="de133-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="de133-110">*учетная запись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de133-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de133-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="de133-111">Type: **UINT**</span></span>

<span data-ttu-id="de133-112">Число извлекаемых контекстных цветов.</span><span class="sxs-lookup"><span data-stu-id="de133-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="de133-113">Это значение должно быть размером или меньше, чем размер, доступный для *ппиколорконтекстс*.</span><span class="sxs-lookup"><span data-stu-id="de133-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="de133-114">*ппиколорконтекстс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="de133-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de133-115">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="de133-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="de133-116">Указатель, получающий указатель на [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="de133-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="de133-117">*пкактуалкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de133-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de133-118">Тип: **uint \***</span><span class="sxs-lookup"><span data-stu-id="de133-118">Type: **UINT\***</span></span>

<span data-ttu-id="de133-119">Указатель, получающий количество цветовых контекстов, содержащихся в изображении.</span><span class="sxs-lookup"><span data-stu-id="de133-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de133-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de133-120">Return value</span></span>

<span data-ttu-id="de133-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de133-121">Type: **HRESULT**</span></span>

<span data-ttu-id="de133-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="de133-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de133-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de133-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de133-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="de133-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="de133-125">Требования</span><span class="sxs-lookup"><span data-stu-id="de133-125">Requirements</span></span>



| <span data-ttu-id="de133-126">Требование</span><span class="sxs-lookup"><span data-stu-id="de133-126">Requirement</span></span> | <span data-ttu-id="de133-127">Значение</span><span class="sxs-lookup"><span data-stu-id="de133-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de133-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de133-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de133-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de133-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="de133-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de133-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de133-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de133-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="de133-132">DLL</span><span class="sxs-lookup"><span data-stu-id="de133-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de133-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de133-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




