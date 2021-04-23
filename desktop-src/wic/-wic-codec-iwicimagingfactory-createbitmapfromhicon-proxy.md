---
description: Функция-посредник для метода Креатебитмапфромхикон.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: Функция IWICImagingFactory_CreateBitmapFromHICON_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702857"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="dc88b-103">IWICImagingFactory \_ креатебитмапфромхикон \_ -функция</span><span class="sxs-lookup"><span data-stu-id="dc88b-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="dc88b-104">Функция-посредник для метода [**креатебитмапфромхикон**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .</span><span class="sxs-lookup"><span data-stu-id="dc88b-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc88b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc88b-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="dc88b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc88b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc88b-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc88b-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc88b-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="dc88b-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="dc88b-109">_hIcon \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="dc88b-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc88b-110">Тип: **Хикон**</span><span class="sxs-lookup"><span data-stu-id="dc88b-110">Type: **HICON**</span></span>

<span data-ttu-id="dc88b-111">Маркер значка для создания нового точечного рисунка из.</span><span class="sxs-lookup"><span data-stu-id="dc88b-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="dc88b-112">*ппибитмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dc88b-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc88b-113">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc88b-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="dc88b-114">Указатель, получающий указатель на новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="dc88b-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc88b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc88b-115">Return value</span></span>

<span data-ttu-id="dc88b-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc88b-116">Type: **HRESULT**</span></span>

<span data-ttu-id="dc88b-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dc88b-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc88b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc88b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc88b-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc88b-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dc88b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dc88b-120">Requirements</span></span>



| <span data-ttu-id="dc88b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dc88b-121">Requirement</span></span> | <span data-ttu-id="dc88b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc88b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc88b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc88b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc88b-124">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc88b-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dc88b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc88b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc88b-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc88b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dc88b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dc88b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc88b-128"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc88b-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




