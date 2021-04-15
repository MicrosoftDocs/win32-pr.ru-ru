---
description: Функция-посредник для метода Жетпикселформат.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Функция IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702400"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="baa1a-103">IWICBitmapSource \_ жетпикселформат \_ -функция</span><span class="sxs-lookup"><span data-stu-id="baa1a-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="baa1a-104">Функция-посредник для метода [**жетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .</span><span class="sxs-lookup"><span data-stu-id="baa1a-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="baa1a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="baa1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="baa1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa1a-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="baa1a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baa1a-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="baa1a-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="baa1a-109">Указатель на этот объект [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="baa1a-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="baa1a-110">*ппикселформат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="baa1a-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="baa1a-111">Тип: \**викпикселформатгуид \** _</span><span class="sxs-lookup"><span data-stu-id="baa1a-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="baa1a-112">Указатель, получающий GUID формата пикселей, в котором хранится битовая карта.</span><span class="sxs-lookup"><span data-stu-id="baa1a-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa1a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baa1a-113">Return value</span></span>

<span data-ttu-id="baa1a-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="baa1a-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="baa1a-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="baa1a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="baa1a-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="baa1a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa1a-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="baa1a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="baa1a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="baa1a-118">Requirements</span></span>



| <span data-ttu-id="baa1a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="baa1a-119">Requirement</span></span> | <span data-ttu-id="baa1a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="baa1a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa1a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="baa1a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="baa1a-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baa1a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="baa1a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="baa1a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="baa1a-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="baa1a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="baa1a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="baa1a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baa1a-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="baa1a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




