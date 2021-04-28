---
description: IWICBitmapDecoder_CopyPalette_Proxy функция-прокси для метода Копипалетте.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: Функция IWICBitmapDecoder_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086362"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="14329-103">Ивикбитмапдекодер \_ копипалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="14329-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="14329-104">Функция-посредник для метода [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="14329-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14329-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14329-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="14329-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14329-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="14329-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14329-108">Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="14329-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="14329-109">Указатель на этот объект [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="14329-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="14329-110">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14329-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14329-111">Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="14329-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="14329-112">Копируемая палитра изображений.</span><span class="sxs-lookup"><span data-stu-id="14329-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14329-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14329-113">Return value</span></span>

<span data-ttu-id="14329-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14329-114">Type: **HRESULT**</span></span>

<span data-ttu-id="14329-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="14329-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14329-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14329-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14329-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="14329-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14329-118">Требования</span><span class="sxs-lookup"><span data-stu-id="14329-118">Requirements</span></span>



| <span data-ttu-id="14329-119">Требование</span><span class="sxs-lookup"><span data-stu-id="14329-119">Requirement</span></span> | <span data-ttu-id="14329-120">Значение</span><span class="sxs-lookup"><span data-stu-id="14329-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14329-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14329-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14329-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14329-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14329-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14329-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14329-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14329-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14329-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14329-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14329-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14329-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




