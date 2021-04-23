---
description: Функция-посредник для метода Сетресолутион.
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
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693172"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="e34ee-103">Ивикбитмапфраминкоде \_ сетресолутион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e34ee-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="e34ee-104">Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="e34ee-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e34ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e34ee-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="e34ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e34ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e34ee-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="e34ee-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e34ee-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="e34ee-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="e34ee-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="e34ee-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="e34ee-110">*дпикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e34ee-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e34ee-111">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="e34ee-111">Type: **double**</span></span>

<span data-ttu-id="e34ee-112">Значение разрешения по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="e34ee-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="e34ee-113">*дпий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e34ee-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e34ee-114">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="e34ee-114">Type: **double**</span></span>

<span data-ttu-id="e34ee-115">Значение разрешения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="e34ee-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e34ee-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e34ee-116">Return value</span></span>

<span data-ttu-id="e34ee-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e34ee-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e34ee-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e34ee-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e34ee-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e34ee-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34ee-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="e34ee-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e34ee-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e34ee-121">Requirements</span></span>



| <span data-ttu-id="e34ee-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e34ee-122">Requirement</span></span> | <span data-ttu-id="e34ee-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e34ee-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e34ee-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e34ee-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e34ee-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e34ee-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e34ee-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e34ee-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e34ee-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e34ee-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e34ee-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e34ee-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e34ee-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e34ee-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




