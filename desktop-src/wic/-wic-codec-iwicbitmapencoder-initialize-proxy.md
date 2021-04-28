---
description: IWICBitmapEncoder_Initialize_Proxy функция-прокси для метода Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: Функция IWICBitmapEncoder_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100622"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="0cb8d-103">Ивикбитмапенкодер \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="0cb8d-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="0cb8d-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) .</span><span class="sxs-lookup"><span data-stu-id="0cb8d-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cb8d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="0cb8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cb8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb8d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="0cb8d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb8d-108">Тип: **[ **ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="0cb8d-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="0cb8d-109">Указатель на этот объект [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="0cb8d-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0cb8d-110">*пистреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cb8d-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb8d-111">Тип: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span><span class="sxs-lookup"><span data-stu-id="0cb8d-111">Type: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span></span>

<span data-ttu-id="0cb8d-112">Выходной поток.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="0cb8d-113">*качеоптион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cb8d-113">*cacheOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb8d-114">Тип: **[ **викбитмапенкодеркачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="0cb8d-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="0cb8d-115">[**Викбитмапенкодеркачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) , используемый при инициализации.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb8d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cb8d-116">Return value</span></span>

<span data-ttu-id="0cb8d-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0cb8d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="0cb8d-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cb8d-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cb8d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb8d-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="0cb8d-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb8d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0cb8d-121">Requirements</span></span>



| <span data-ttu-id="0cb8d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0cb8d-122">Requirement</span></span> | <span data-ttu-id="0cb8d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0cb8d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb8d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cb8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb8d-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0cb8d-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0cb8d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cb8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb8d-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0cb8d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0cb8d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb8d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb8d-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cb8d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

