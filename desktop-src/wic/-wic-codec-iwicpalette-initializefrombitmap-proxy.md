---
description: Функция-посредник для метода Инитиализефромбитмап.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: Функция IWICPalette_InitializeFromBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703271"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="14b79-103">Ивикпалетте \_ инитиализефромбитмап \_ -функция</span><span class="sxs-lookup"><span data-stu-id="14b79-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="14b79-104">Функция-посредник для метода [**инитиализефромбитмап**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) .</span><span class="sxs-lookup"><span data-stu-id="14b79-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14b79-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="14b79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b79-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="14b79-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b79-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="14b79-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="14b79-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="14b79-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="14b79-110">*писурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14b79-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b79-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="14b79-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="14b79-112">Указатель на исходное растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="14b79-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="14b79-113">_colorCount \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="14b79-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b79-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="14b79-114">Type: **UINT**</span></span>

<span data-ttu-id="14b79-115">Число цветов для инициализации палитры.</span><span class="sxs-lookup"><span data-stu-id="14b79-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="14b79-116">*фаддтранспарентколор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14b79-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b79-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="14b79-117">Type: **BOOL**</span></span>

<span data-ttu-id="14b79-118">Значение, указывающее, следует ли добавить прозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="14b79-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b79-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b79-119">Return value</span></span>

<span data-ttu-id="14b79-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14b79-120">Type: **HRESULT**</span></span>

<span data-ttu-id="14b79-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="14b79-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14b79-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14b79-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b79-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="14b79-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14b79-124">Требования</span><span class="sxs-lookup"><span data-stu-id="14b79-124">Requirements</span></span>



| <span data-ttu-id="14b79-125">Требование</span><span class="sxs-lookup"><span data-stu-id="14b79-125">Requirement</span></span> | <span data-ttu-id="14b79-126">Значение</span><span class="sxs-lookup"><span data-stu-id="14b79-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b79-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14b79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14b79-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14b79-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14b79-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14b79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14b79-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14b79-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14b79-131">DLL</span><span class="sxs-lookup"><span data-stu-id="14b79-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b79-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14b79-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




