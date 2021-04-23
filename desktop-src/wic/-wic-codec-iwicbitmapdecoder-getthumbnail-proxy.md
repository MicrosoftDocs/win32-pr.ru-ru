---
description: Функция-посредник для метода "Thumbnail".
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: Функция IWICBitmapDecoder_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7412999b1a685c0188e0f277e073791d753a245b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693763"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="de43a-103">\_ \_ Функция Ивикбитмапдекодер-эскиза</span><span class="sxs-lookup"><span data-stu-id="de43a-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="de43a-104">Функция-посредник для метода " [**thumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) ".</span><span class="sxs-lookup"><span data-stu-id="de43a-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de43a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de43a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="de43a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de43a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de43a-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="de43a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de43a-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="de43a-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="de43a-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="de43a-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="de43a-110">*пписумбнаил* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de43a-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de43a-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="de43a-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="de43a-112">Указатель, получающий указатель на [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) эскиза.</span><span class="sxs-lookup"><span data-stu-id="de43a-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de43a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de43a-113">Return value</span></span>

<span data-ttu-id="de43a-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de43a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="de43a-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="de43a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de43a-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de43a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de43a-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="de43a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="de43a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="de43a-118">Requirements</span></span>



| <span data-ttu-id="de43a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="de43a-119">Requirement</span></span> | <span data-ttu-id="de43a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="de43a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de43a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de43a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de43a-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de43a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="de43a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de43a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de43a-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de43a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="de43a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de43a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de43a-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de43a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




