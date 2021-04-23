---
description: Функция-посредник для метода Инитиализефромпалетте.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: Функция IWICPalette_InitializeFromPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912627"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="4fbac-103">Ивикпалетте \_ инитиализефромпалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="4fbac-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="4fbac-104">Функция-посредник для метода [**инитиализефромпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .</span><span class="sxs-lookup"><span data-stu-id="4fbac-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fbac-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="4fbac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fbac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fbac-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="4fbac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbac-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="4fbac-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="4fbac-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="4fbac-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="4fbac-110">*пимилпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fbac-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbac-111">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="4fbac-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="4fbac-112">Указатель на исходную палитру.</span><span class="sxs-lookup"><span data-stu-id="4fbac-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fbac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fbac-113">Return value</span></span>

<span data-ttu-id="4fbac-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4fbac-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4fbac-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4fbac-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4fbac-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4fbac-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbac-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="4fbac-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbac-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4fbac-118">Requirements</span></span>



| <span data-ttu-id="4fbac-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4fbac-119">Requirement</span></span> | <span data-ttu-id="4fbac-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4fbac-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbac-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fbac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbac-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fbac-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4fbac-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fbac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbac-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4fbac-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4fbac-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4fbac-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fbac-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fbac-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




