---
description: IWICBitmapFrameDecode_GetColorContexts_Proxy функция-прокси для метода Жетколорконтекстс.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: Функция IWICBitmapFrameDecode_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100582"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="3f5bc-103">IWICBitmapFrameDecode \_ жетколорконтекстс \_ -функция</span><span class="sxs-lookup"><span data-stu-id="3f5bc-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="3f5bc-104">Функция-посредник для метода [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="3f5bc-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f5bc-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="3f5bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f5bc-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f5bc-108">Тип: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="3f5bc-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="3f5bc-109">Указатель на этот объект [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="3f5bc-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f5bc-110">*учетная запись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f5bc-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f5bc-111">Type: **UINT**</span></span>

<span data-ttu-id="3f5bc-112">Число извлекаемых контекстных цветов.</span><span class="sxs-lookup"><span data-stu-id="3f5bc-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="3f5bc-113">Это значение должно быть размером или меньше, чем размер, доступный для *ппиколорконтекстс*.</span><span class="sxs-lookup"><span data-stu-id="3f5bc-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="3f5bc-114">*ппиколорконтекстс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f5bc-115">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="3f5bc-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="3f5bc-116">Указатель, получающий указатель на объекты [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .</span><span class="sxs-lookup"><span data-stu-id="3f5bc-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="3f5bc-117">*пкактуалкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f5bc-118">Тип: **uint \***</span><span class="sxs-lookup"><span data-stu-id="3f5bc-118">Type: **UINT\***</span></span>

<span data-ttu-id="3f5bc-119">Указатель, получающий количество цветовых контекстов, содержащихся в кадре изображения.</span><span class="sxs-lookup"><span data-stu-id="3f5bc-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f5bc-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f5bc-120">Return value</span></span>

<span data-ttu-id="3f5bc-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3f5bc-121">Type: **HRESULT**</span></span>

<span data-ttu-id="3f5bc-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3f5bc-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f5bc-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f5bc-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f5bc-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="3f5bc-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5bc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3f5bc-125">Requirements</span></span>



| <span data-ttu-id="3f5bc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3f5bc-126">Requirement</span></span> | <span data-ttu-id="3f5bc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3f5bc-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5bc-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f5bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5bc-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3f5bc-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f5bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5bc-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f5bc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3f5bc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f5bc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f5bc-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f5bc-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




