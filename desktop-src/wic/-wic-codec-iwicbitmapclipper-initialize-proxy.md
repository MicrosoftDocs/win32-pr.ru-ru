---
description: IWICBitmapClipper_Initialize_Proxy функция-прокси для метода Initialize.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: Функция IWICBitmapClipper_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086392"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="3b9a3-103">Ивикбитмапклиппер \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="3b9a3-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="3b9a3-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b9a3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="3b9a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b9a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b9a3-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="3b9a3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9a3-108">Тип: **[ **ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="3b9a3-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="3b9a3-109">Указатель на этот объект [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b9a3-110">*писаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b9a3-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9a3-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="3b9a3-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="3b9a3-112">Источник входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="3b9a3-113">*КНР* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b9a3-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9a3-114">Тип: **const [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="3b9a3-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="3b9a3-115">Прямоугольник исходного растрового изображения для обрезки.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b9a3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b9a3-116">Return value</span></span>

<span data-ttu-id="3b9a3-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b9a3-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3b9a3-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b9a3-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9a3-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="3b9a3-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3b9a3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3b9a3-121">Requirements</span></span>



| <span data-ttu-id="3b9a3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3b9a3-122">Requirement</span></span> | <span data-ttu-id="3b9a3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3b9a3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9a3-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b9a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3b9a3-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b9a3-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3b9a3-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b9a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3b9a3-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b9a3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3b9a3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3b9a3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b9a3-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b9a3-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




