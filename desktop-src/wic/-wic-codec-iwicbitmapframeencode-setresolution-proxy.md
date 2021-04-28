---
description: IWICBitmapFrameEncode_SetResolution_Proxy функция-прокси для метода Сетресолутион.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: Функция IWICBitmapFrameEncode_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116612"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="0cab6-103">Ивикбитмапфраминкоде \_ сетресолутион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="0cab6-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="0cab6-104">Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="0cab6-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cab6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cab6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="0cab6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cab6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cab6-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="0cab6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cab6-108">Тип: **[ **ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="0cab6-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="0cab6-109">Указатель на этот объект [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="0cab6-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="0cab6-110">*дпикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cab6-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cab6-111">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="0cab6-111">Type: **double**</span></span>

<span data-ttu-id="0cab6-112">Значение разрешения по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="0cab6-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="0cab6-113">*дпий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cab6-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cab6-114">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="0cab6-114">Type: **double**</span></span>

<span data-ttu-id="0cab6-115">Значение разрешения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="0cab6-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cab6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cab6-116">Return value</span></span>

<span data-ttu-id="0cab6-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0cab6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="0cab6-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cab6-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cab6-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cab6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cab6-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="0cab6-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0cab6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0cab6-121">Requirements</span></span>



| <span data-ttu-id="0cab6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0cab6-122">Requirement</span></span> | <span data-ttu-id="0cab6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0cab6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cab6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cab6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0cab6-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0cab6-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0cab6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cab6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0cab6-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0cab6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0cab6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0cab6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cab6-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cab6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




