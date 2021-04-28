---
description: IWICBitmapFrameDecode_GetThumbnail_Proxy функция-прокси для метода с параметром thumbnail.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: Функция IWICBitmapFrameDecode_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7f3c94461ac13aa39d14b97f13fe5e9e8d7569a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113642"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="b9fcd-103">\_ \_ Функция IWICBitmapFrameDecode-эскиза</span><span class="sxs-lookup"><span data-stu-id="b9fcd-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="b9fcd-104">Функция-посредник для метода " [**thumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) ".</span><span class="sxs-lookup"><span data-stu-id="b9fcd-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fcd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9fcd-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="b9fcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9fcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9fcd-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="b9fcd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9fcd-108">Тип: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="b9fcd-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="b9fcd-109">Указатель на этот объект [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="b9fcd-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcd-110">*пписумбнаил* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b9fcd-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9fcd-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b9fcd-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="b9fcd-112">Указатель, получающий указатель на [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) эскиза.</span><span class="sxs-lookup"><span data-stu-id="b9fcd-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9fcd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9fcd-113">Return value</span></span>

<span data-ttu-id="b9fcd-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9fcd-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b9fcd-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b9fcd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9fcd-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9fcd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9fcd-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="b9fcd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b9fcd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b9fcd-118">Requirements</span></span>



| <span data-ttu-id="b9fcd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b9fcd-119">Requirement</span></span> | <span data-ttu-id="b9fcd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b9fcd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9fcd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9fcd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fcd-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9fcd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b9fcd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9fcd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fcd-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9fcd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b9fcd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9fcd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9fcd-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9fcd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




