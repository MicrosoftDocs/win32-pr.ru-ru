---
description: Функция-посредник для метода Хасалфа.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: Функция IWICPalette_HasAlpha_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998933"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="6195f-103">Ивикпалетте \_ хасалфа \_ -функция</span><span class="sxs-lookup"><span data-stu-id="6195f-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="6195f-104">Функция-посредник для метода [**хасалфа**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .</span><span class="sxs-lookup"><span data-stu-id="6195f-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6195f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6195f-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="6195f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6195f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6195f-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="6195f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6195f-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="6195f-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="6195f-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="6195f-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="6195f-110">*пфхасалфа* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6195f-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6195f-111">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="6195f-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="6195f-112">Указатель, который получает, `TRUE` Если палитра содержит прозрачный цвет. в противном случае — значение `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="6195f-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6195f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6195f-113">Return value</span></span>

<span data-ttu-id="6195f-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6195f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6195f-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6195f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6195f-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6195f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6195f-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="6195f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6195f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6195f-118">Requirements</span></span>



| <span data-ttu-id="6195f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6195f-119">Requirement</span></span> | <span data-ttu-id="6195f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6195f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6195f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6195f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6195f-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6195f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6195f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6195f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6195f-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6195f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6195f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6195f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6195f-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6195f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




