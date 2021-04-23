---
description: Функция-посредник для метода Креатебитмапклиппер.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: Функция IWICImagingFactory_CreateBitmapClipper_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999256"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="77c2d-103">IWICImagingFactory \_ креатебитмапклиппер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="77c2d-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="77c2d-104">Функция-посредник для метода [**креатебитмапклиппер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="77c2d-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77c2d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="77c2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c2d-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77c2d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c2d-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="77c2d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="77c2d-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77c2d-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77c2d-110">Тип: **[ **ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="77c2d-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="77c2d-111">Указатель, получающий указатель на новый [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span><span class="sxs-lookup"><span data-stu-id="77c2d-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c2d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77c2d-112">Return value</span></span>

<span data-ttu-id="77c2d-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="77c2d-113">Type: **HRESULT**</span></span>

<span data-ttu-id="77c2d-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="77c2d-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77c2d-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77c2d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c2d-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="77c2d-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="77c2d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="77c2d-117">Requirements</span></span>



| <span data-ttu-id="77c2d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="77c2d-118">Requirement</span></span> | <span data-ttu-id="77c2d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="77c2d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77c2d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77c2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77c2d-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77c2d-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="77c2d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77c2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77c2d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77c2d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="77c2d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="77c2d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77c2d-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77c2d-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




