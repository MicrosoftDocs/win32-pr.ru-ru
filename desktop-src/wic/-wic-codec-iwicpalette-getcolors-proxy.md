---
description: Функция-посредник для метода "Colors".
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Функция IWICPalette_GetColors_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265450"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="4cb7d-103">\_ \_ Функция прокси-сервера Ивикпалеттеных цветов</span><span class="sxs-lookup"><span data-stu-id="4cb7d-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="4cb7d-104">Функция-посредник для метода " [**Colors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) ".</span><span class="sxs-lookup"><span data-stu-id="4cb7d-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cb7d-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="4cb7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cb7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb7d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb7d-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="4cb7d-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="4cb7d-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="4cb7d-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="4cb7d-110">*колоркаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb7d-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="4cb7d-111">Type: **UINT**</span></span>

<span data-ttu-id="4cb7d-112">Размер массива *пколорс* .</span><span class="sxs-lookup"><span data-stu-id="4cb7d-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="4cb7d-113">*пколорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb7d-114">Тип: \**викколор \** _</span><span class="sxs-lookup"><span data-stu-id="4cb7d-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="4cb7d-115">Указатель, получающий цвета палитры.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="4cb7d-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb7d-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="4cb7d-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="4cb7d-118">Фактический размер, необходимый для получения цветов палитры.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb7d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cb7d-119">Return value</span></span>

<span data-ttu-id="4cb7d-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4cb7d-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4cb7d-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4cb7d-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cb7d-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cb7d-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="4cb7d-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb7d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4cb7d-124">Requirements</span></span>



| <span data-ttu-id="4cb7d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4cb7d-125">Requirement</span></span> | <span data-ttu-id="4cb7d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4cb7d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb7d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cb7d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb7d-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4cb7d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cb7d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb7d-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cb7d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4cb7d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb7d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb7d-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cb7d-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




