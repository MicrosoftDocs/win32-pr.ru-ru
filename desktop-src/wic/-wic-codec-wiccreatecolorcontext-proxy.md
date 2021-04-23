---
description: Функция-посредник для создания Ивикколорконтекст.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: Функция WICCreateColorContext_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702392"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="77e30-103">Виккреатеколорконтекст \_ -функция прокси</span><span class="sxs-lookup"><span data-stu-id="77e30-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="77e30-104">Функция-посредник для создания [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="77e30-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="77e30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77e30-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="77e30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77e30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e30-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="77e30-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e30-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="77e30-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="77e30-109">Указатель на этот объект [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="77e30-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="77e30-110">*ппиколорконтекст*</span><span class="sxs-lookup"><span data-stu-id="77e30-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="77e30-111">Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="77e30-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e30-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77e30-112">Return value</span></span>

<span data-ttu-id="77e30-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="77e30-113">Type: **HRESULT**</span></span>

<span data-ttu-id="77e30-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="77e30-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77e30-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77e30-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77e30-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="77e30-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="77e30-117">Требования</span><span class="sxs-lookup"><span data-stu-id="77e30-117">Requirements</span></span>



| <span data-ttu-id="77e30-118">Требование</span><span class="sxs-lookup"><span data-stu-id="77e30-118">Requirement</span></span> | <span data-ttu-id="77e30-119">Значение</span><span class="sxs-lookup"><span data-stu-id="77e30-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e30-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77e30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77e30-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77e30-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="77e30-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77e30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77e30-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77e30-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="77e30-124">DLL</span><span class="sxs-lookup"><span data-stu-id="77e30-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e30-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77e30-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




