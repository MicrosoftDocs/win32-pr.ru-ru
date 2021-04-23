---
description: Функция-посредник для метода Жетбитсперпиксел.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: Функция IWICPixelFormatInfo_GetBitsPerPixel_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712617"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="804db-103">Ивикпикселформатинфо \_ жетбитсперпиксел \_ -функция</span><span class="sxs-lookup"><span data-stu-id="804db-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="804db-104">Функция-посредник для метода [**жетбитсперпиксел**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .</span><span class="sxs-lookup"><span data-stu-id="804db-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="804db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="804db-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="804db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="804db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="804db-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="804db-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="804db-108">Тип: \**[**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="804db-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="804db-109">Указатель на этот объект [_ *ивикпикселформатинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="804db-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="804db-110">*пуибитсперпиксел* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="804db-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="804db-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="804db-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="804db-112">Указатель, получающий пиксель формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="804db-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="804db-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="804db-113">Return value</span></span>

<span data-ttu-id="804db-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="804db-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="804db-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="804db-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="804db-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="804db-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="804db-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="804db-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="804db-118">Требования</span><span class="sxs-lookup"><span data-stu-id="804db-118">Requirements</span></span>



| <span data-ttu-id="804db-119">Требование</span><span class="sxs-lookup"><span data-stu-id="804db-119">Requirement</span></span> | <span data-ttu-id="804db-120">Значение</span><span class="sxs-lookup"><span data-stu-id="804db-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804db-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="804db-121">Minimum supported client</span></span><br/> | <span data-ttu-id="804db-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="804db-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="804db-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="804db-123">Minimum supported server</span></span><br/> | <span data-ttu-id="804db-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="804db-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="804db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="804db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="804db-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="804db-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




