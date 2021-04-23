---
description: Функция-посредник для метода методом Resize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Функция IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702401"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="4ce46-103">IWICBitmapSource \_ \_ -функция @ size</span><span class="sxs-lookup"><span data-stu-id="4ce46-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="4ce46-104">Функция-посредник для метода методом [**resize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .</span><span class="sxs-lookup"><span data-stu-id="4ce46-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ce46-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="4ce46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ce46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce46-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="4ce46-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce46-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="4ce46-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="4ce46-109">Указатель на этот объект [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="4ce46-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="4ce46-110">*пуивидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ce46-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce46-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="4ce46-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="4ce46-112">Указатель, получающий ширину точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4ce46-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="4ce46-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ce46-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce46-114">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="4ce46-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="4ce46-115">Указатель, который получает высоту точечного рисунка в пикселях</span><span class="sxs-lookup"><span data-stu-id="4ce46-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce46-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ce46-116">Return value</span></span>

<span data-ttu-id="4ce46-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4ce46-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4ce46-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ce46-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ce46-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ce46-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce46-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="4ce46-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce46-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4ce46-121">Requirements</span></span>



| <span data-ttu-id="4ce46-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4ce46-122">Requirement</span></span> | <span data-ttu-id="4ce46-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4ce46-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce46-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ce46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce46-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ce46-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4ce46-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ce46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce46-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ce46-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4ce46-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce46-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ce46-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ce46-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




