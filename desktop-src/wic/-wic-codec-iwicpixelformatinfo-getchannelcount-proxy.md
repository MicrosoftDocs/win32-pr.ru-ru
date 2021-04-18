---
description: Функция-посредник для метода Жетчаннелкаунт.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: Функция IWICPixelFormatInfo_GetChannelCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693760"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="c8feb-103">Ивикпикселформатинфо \_ жетчаннелкаунт \_ -функция</span><span class="sxs-lookup"><span data-stu-id="c8feb-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="c8feb-104">Функция-посредник для метода [**жетчаннелкаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .</span><span class="sxs-lookup"><span data-stu-id="c8feb-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8feb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8feb-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="c8feb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8feb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8feb-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="c8feb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8feb-108">Тип: \**[**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c8feb-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="c8feb-109">Указатель на этот объект [_ *ивикпикселформатинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="c8feb-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8feb-110">*пуичаннелкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8feb-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8feb-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c8feb-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="c8feb-112">Указатель, получающий число каналов.</span><span class="sxs-lookup"><span data-stu-id="c8feb-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8feb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8feb-113">Return value</span></span>

<span data-ttu-id="c8feb-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c8feb-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c8feb-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c8feb-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8feb-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8feb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8feb-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8feb-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8feb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c8feb-118">Requirements</span></span>



| <span data-ttu-id="c8feb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c8feb-119">Requirement</span></span> | <span data-ttu-id="c8feb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c8feb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8feb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8feb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8feb-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8feb-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8feb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8feb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8feb-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8feb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8feb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c8feb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8feb-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8feb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




