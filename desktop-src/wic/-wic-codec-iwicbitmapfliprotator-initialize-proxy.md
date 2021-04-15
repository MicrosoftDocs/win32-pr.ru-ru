---
description: Функция-посредник для метода Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: Функция IWICBitmapFlipRotator_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701441"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="4a438-103">Ивикбитмапфлипротатор \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="4a438-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="4a438-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="4a438-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a438-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a438-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="4a438-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a438-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a438-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="4a438-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a438-108">Тип: \**[**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="4a438-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="4a438-109">Указатель на этот объект [_ *ивикбитмапфлипротатор* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="4a438-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="4a438-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a438-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a438-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="4a438-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="4a438-112">Источник входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="4a438-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="4a438-113">_options \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4a438-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a438-114">Тип: **[ **викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="4a438-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="4a438-115">[**Викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) для отражения или поворота изображения.</span><span class="sxs-lookup"><span data-stu-id="4a438-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a438-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a438-116">Return value</span></span>

<span data-ttu-id="4a438-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a438-117">Type: **HRESULT**</span></span>

<span data-ttu-id="4a438-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4a438-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a438-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a438-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a438-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="4a438-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4a438-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4a438-121">Requirements</span></span>



| <span data-ttu-id="4a438-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4a438-122">Requirement</span></span> | <span data-ttu-id="4a438-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4a438-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a438-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a438-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a438-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a438-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4a438-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a438-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a438-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a438-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4a438-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4a438-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a438-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a438-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




