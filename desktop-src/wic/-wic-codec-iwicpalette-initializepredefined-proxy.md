---
description: Функция-посредник для метода Инитиализепредефинед.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: Функция IWICPalette_InitializePredefined_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816824"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="66435-103">Ивикпалетте \_ инитиализепредефинед \_ -функция</span><span class="sxs-lookup"><span data-stu-id="66435-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="66435-104">Функция-посредник для метода [**инитиализепредефинед**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .</span><span class="sxs-lookup"><span data-stu-id="66435-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66435-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66435-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="66435-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66435-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="66435-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66435-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="66435-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="66435-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="66435-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="66435-110">*епалеттетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66435-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66435-111">Тип: **[ **викбитмаппалеттетипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="66435-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="66435-112">Требуемый предварительно определенный тип палитры.</span><span class="sxs-lookup"><span data-stu-id="66435-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="66435-113">*фаддтранспарентколор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66435-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66435-114">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="66435-114">Type: **BOOL**</span></span>

<span data-ttu-id="66435-115">Необязательный цвет транпарент для добавления к палитре.</span><span class="sxs-lookup"><span data-stu-id="66435-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="66435-116">Если прозрачный цвет не требуется, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="66435-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66435-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66435-117">Return value</span></span>

<span data-ttu-id="66435-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="66435-118">Type: **HRESULT**</span></span>

<span data-ttu-id="66435-119">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="66435-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66435-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66435-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="66435-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="66435-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="66435-122">Требования</span><span class="sxs-lookup"><span data-stu-id="66435-122">Requirements</span></span>



| <span data-ttu-id="66435-123">Требование</span><span class="sxs-lookup"><span data-stu-id="66435-123">Requirement</span></span> | <span data-ttu-id="66435-124">Значение</span><span class="sxs-lookup"><span data-stu-id="66435-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66435-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66435-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66435-126">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66435-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="66435-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66435-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66435-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66435-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="66435-129">DLL</span><span class="sxs-lookup"><span data-stu-id="66435-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66435-130"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66435-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




