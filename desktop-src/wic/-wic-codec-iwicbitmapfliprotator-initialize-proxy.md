---
description: IWICBitmapFlipRotator_Initialize_Proxy функция-прокси для метода Initialize.
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
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091162"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="496f2-103">Ивикбитмапфлипротатор \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="496f2-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="496f2-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="496f2-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="496f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="496f2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="496f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="496f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496f2-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="496f2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496f2-108">Тип: **[ **ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="496f2-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="496f2-109">Указатель на этот объект [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="496f2-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="496f2-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="496f2-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496f2-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="496f2-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="496f2-112">Источник входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="496f2-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="496f2-113">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="496f2-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496f2-114">Тип: **[ **викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="496f2-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="496f2-115">[**Викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) для отражения или поворота изображения.</span><span class="sxs-lookup"><span data-stu-id="496f2-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496f2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="496f2-116">Return value</span></span>

<span data-ttu-id="496f2-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="496f2-117">Type: **HRESULT**</span></span>

<span data-ttu-id="496f2-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="496f2-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="496f2-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="496f2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="496f2-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="496f2-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="496f2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="496f2-121">Requirements</span></span>



| <span data-ttu-id="496f2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="496f2-122">Requirement</span></span> | <span data-ttu-id="496f2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="496f2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496f2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="496f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="496f2-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="496f2-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="496f2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="496f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="496f2-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="496f2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="496f2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="496f2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="496f2-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="496f2-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




