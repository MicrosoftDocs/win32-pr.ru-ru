---
description: Функция-посредник для метода GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: Функция IWICPalette_GetType_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712353"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="f04bc-103">Ивикпалетте \_ \_ -функция GetType</span><span class="sxs-lookup"><span data-stu-id="f04bc-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="f04bc-104">Функция-посредник для метода [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .</span><span class="sxs-lookup"><span data-stu-id="f04bc-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f04bc-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="f04bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f04bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04bc-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="f04bc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bc-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="f04bc-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="f04bc-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="f04bc-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="f04bc-110">*пепалеттетипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f04bc-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bc-111">Тип: \**[**викбитмаппалеттетипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="f04bc-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="f04bc-112">Указатель, получающий тип палитры бимтап.</span><span class="sxs-lookup"><span data-stu-id="f04bc-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04bc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f04bc-113">Return value</span></span>

<span data-ttu-id="f04bc-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f04bc-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f04bc-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f04bc-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f04bc-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f04bc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f04bc-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="f04bc-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f04bc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f04bc-118">Requirements</span></span>



| <span data-ttu-id="f04bc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f04bc-119">Requirement</span></span> | <span data-ttu-id="f04bc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f04bc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04bc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f04bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f04bc-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f04bc-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f04bc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f04bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f04bc-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f04bc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f04bc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f04bc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f04bc-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f04bc-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




