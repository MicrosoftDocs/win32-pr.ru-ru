---
description: IWICBitmap_SetResolution_Proxy функция-прокси для метода Сетресолутион.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: Функция IWICBitmap_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086382"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="43757-103">Ивикбитмап \_ сетресолутион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="43757-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="43757-104">Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="43757-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43757-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43757-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="43757-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43757-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="43757-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43757-108">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="43757-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="43757-109">Указатель на этот объект [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="43757-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="43757-110">*дпикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43757-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43757-111">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="43757-111">Type: **double**</span></span>

<span data-ttu-id="43757-112">Разрешение по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="43757-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="43757-113">*дпий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43757-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43757-114">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="43757-114">Type: **double**</span></span>

<span data-ttu-id="43757-115">Разрешение по вертикали.</span><span class="sxs-lookup"><span data-stu-id="43757-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43757-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43757-116">Return value</span></span>

<span data-ttu-id="43757-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43757-117">Type: **HRESULT**</span></span>

<span data-ttu-id="43757-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="43757-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43757-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43757-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43757-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="43757-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="43757-121">Требования</span><span class="sxs-lookup"><span data-stu-id="43757-121">Requirements</span></span>



| <span data-ttu-id="43757-122">Требование</span><span class="sxs-lookup"><span data-stu-id="43757-122">Requirement</span></span> | <span data-ttu-id="43757-123">Значение</span><span class="sxs-lookup"><span data-stu-id="43757-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43757-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43757-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43757-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43757-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="43757-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43757-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43757-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43757-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="43757-128">DLL</span><span class="sxs-lookup"><span data-stu-id="43757-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43757-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43757-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




