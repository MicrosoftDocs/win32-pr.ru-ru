---
description: Функция-посредник для метода Инитиализекустом.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: Функция IWICPalette_InitializeCustom_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712693"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="2cf92-103">Ивикпалетте \_ инитиализекустом \_ -функция</span><span class="sxs-lookup"><span data-stu-id="2cf92-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="2cf92-104">Функция-посредник для метода [**инитиализекустом**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .</span><span class="sxs-lookup"><span data-stu-id="2cf92-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cf92-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="2cf92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cf92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf92-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf92-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="2cf92-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="2cf92-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="2cf92-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="2cf92-110">*пколорс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf92-111">Тип: \**викколор \** _</span><span class="sxs-lookup"><span data-stu-id="2cf92-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="2cf92-112">Указатель на массив цветов.</span><span class="sxs-lookup"><span data-stu-id="2cf92-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="2cf92-113">_colorCount \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf92-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="2cf92-114">Type: **UINT**</span></span>

<span data-ttu-id="2cf92-115">Число цветов в *пколорс*.</span><span class="sxs-lookup"><span data-stu-id="2cf92-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf92-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cf92-116">Return value</span></span>

<span data-ttu-id="2cf92-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2cf92-117">Type: **HRESULT**</span></span>

<span data-ttu-id="2cf92-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2cf92-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cf92-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2cf92-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf92-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="2cf92-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf92-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2cf92-121">Requirements</span></span>



| <span data-ttu-id="2cf92-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2cf92-122">Requirement</span></span> | <span data-ttu-id="2cf92-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2cf92-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf92-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cf92-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf92-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2cf92-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cf92-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf92-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2cf92-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2cf92-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf92-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




