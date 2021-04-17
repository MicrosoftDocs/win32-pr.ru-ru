---
description: Функция-посредник для метода Доессуппортаниматион.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: Функция IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710975"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="27b1c-103">ИвикбитмапкодеЦинфо \_ доессуппортаниматион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="27b1c-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="27b1c-104">Функция-посредник для метода [**доессуппортаниматион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) .</span><span class="sxs-lookup"><span data-stu-id="27b1c-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27b1c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="27b1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b1c-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="27b1c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27b1c-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="27b1c-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="27b1c-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="27b1c-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="27b1c-110">*пфсуппортаниматион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27b1c-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27b1c-111">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="27b1c-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="27b1c-112">Указатель, получающий \*значение _ true\*\*, если кодек поддерживает изображения со сведениями о времени; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="27b1c-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b1c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27b1c-113">Return value</span></span>

<span data-ttu-id="27b1c-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27b1c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="27b1c-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="27b1c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27b1c-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27b1c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b1c-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="27b1c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="27b1c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="27b1c-118">Requirements</span></span>



| <span data-ttu-id="27b1c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="27b1c-119">Requirement</span></span> | <span data-ttu-id="27b1c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="27b1c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b1c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27b1c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27b1c-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27b1c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="27b1c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27b1c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27b1c-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27b1c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="27b1c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="27b1c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27b1c-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27b1c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




