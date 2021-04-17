---
description: 'Функция прокси компонента Windows Imaging Component (WIC) для Иенумстринг:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: Функция IEnumString_Reset_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710977"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="d1881-103">Иенумстринг \_ Сброс \_ \_ функции прокси-сервера WIC</span><span class="sxs-lookup"><span data-stu-id="d1881-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="d1881-104">Функция прокси компонента Windows Imaging Component (WIC) для Иенумстринг:: Reset.</span><span class="sxs-lookup"><span data-stu-id="d1881-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1881-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1881-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d1881-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1881-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="d1881-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-108">Тип: \**иенумстринг \** _</span><span class="sxs-lookup"><span data-stu-id="d1881-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="d1881-109">парамдеск</span><span class="sxs-lookup"><span data-stu-id="d1881-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="d1881-110">_celt \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d1881-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-111">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="d1881-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="d1881-112">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1881-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-113">Тип: \**лполестр \** _</span><span class="sxs-lookup"><span data-stu-id="d1881-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="d1881-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1881-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-115">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="d1881-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1881-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1881-116">Return value</span></span>

<span data-ttu-id="d1881-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d1881-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d1881-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d1881-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1881-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1881-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1881-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1881-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d1881-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d1881-121">Requirements</span></span>



| <span data-ttu-id="d1881-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d1881-122">Requirement</span></span> | <span data-ttu-id="d1881-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d1881-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1881-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1881-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1881-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1881-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d1881-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1881-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1881-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1881-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d1881-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d1881-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1881-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1881-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




