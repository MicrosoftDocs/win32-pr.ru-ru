---
description: Функция-посредник для метода Вритесаурце.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: Функция IWICBitmapFrameEncode_WriteSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272967"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="28eea-103">Ивикбитмапфраминкоде \_ вритесаурце \_ -функция</span><span class="sxs-lookup"><span data-stu-id="28eea-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="28eea-104">Функция-посредник для метода [**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="28eea-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28eea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28eea-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="28eea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28eea-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="28eea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28eea-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="28eea-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="28eea-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="28eea-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="28eea-110">*пибитмапсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28eea-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28eea-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="28eea-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="28eea-112">Источник точечного рисунка для кодирования.</span><span class="sxs-lookup"><span data-stu-id="28eea-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="28eea-113">_prc \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="28eea-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28eea-114">Тип: \**[**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="28eea-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="28eea-115">Прямоугольник размера источника точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="28eea-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28eea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28eea-116">Return value</span></span>

<span data-ttu-id="28eea-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28eea-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28eea-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="28eea-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28eea-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28eea-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28eea-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="28eea-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28eea-121">Требования</span><span class="sxs-lookup"><span data-stu-id="28eea-121">Requirements</span></span>



| <span data-ttu-id="28eea-122">Требование</span><span class="sxs-lookup"><span data-stu-id="28eea-122">Requirement</span></span> | <span data-ttu-id="28eea-123">Значение</span><span class="sxs-lookup"><span data-stu-id="28eea-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28eea-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28eea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="28eea-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28eea-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28eea-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28eea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="28eea-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28eea-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28eea-128">DLL</span><span class="sxs-lookup"><span data-stu-id="28eea-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28eea-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28eea-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




