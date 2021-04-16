---
description: 'Функция прокси компонента Windows Imaging Component (WIC) для IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: Функция IPropertyBag2_Write_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343252"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="6fcc4-103">IPropertyBag2 \_ \_ -функция записи</span><span class="sxs-lookup"><span data-stu-id="6fcc4-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="6fcc4-104">Функция прокси компонента Windows Imaging Component (WIC) для IPropertyBag2:: Write.</span><span class="sxs-lookup"><span data-stu-id="6fcc4-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fcc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fcc4-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="6fcc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fcc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fcc4-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcc4-108">Тип: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="6fcc4-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="6fcc4-109">парамдеск</span><span class="sxs-lookup"><span data-stu-id="6fcc4-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="6fcc4-110">_cProperties \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcc4-111">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="6fcc4-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="6fcc4-112">*ппропбаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcc4-113">Тип: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="6fcc4-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="6fcc4-114">_pvarValue \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcc4-115">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="6fcc4-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fcc4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fcc4-116">Return value</span></span>

<span data-ttu-id="6fcc4-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6fcc4-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6fcc4-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6fcc4-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fcc4-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fcc4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcc4-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="6fcc4-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcc4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6fcc4-121">Requirements</span></span>



| <span data-ttu-id="6fcc4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6fcc4-122">Requirement</span></span> | <span data-ttu-id="6fcc4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6fcc4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcc4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fcc4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcc4-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6fcc4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fcc4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcc4-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6fcc4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6fcc4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fcc4-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fcc4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

