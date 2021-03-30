---
description: Функция-посредник для метода Жетфрамекаунт.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: Функция IWICBitmapDecoder_GetFrameCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809580"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="61f99-103">Ивикбитмапдекодер \_ жетфрамекаунт \_ -функция</span><span class="sxs-lookup"><span data-stu-id="61f99-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="61f99-104">Функция-посредник для метода [**жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="61f99-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61f99-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="61f99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61f99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f99-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="61f99-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61f99-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="61f99-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="61f99-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="61f99-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="61f99-110">*pCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61f99-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61f99-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="61f99-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="61f99-112">Указатель, получающий общее число кадров в изображении.</span><span class="sxs-lookup"><span data-stu-id="61f99-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f99-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61f99-113">Return value</span></span>

<span data-ttu-id="61f99-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="61f99-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="61f99-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="61f99-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61f99-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61f99-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f99-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="61f99-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="61f99-118">Требования</span><span class="sxs-lookup"><span data-stu-id="61f99-118">Requirements</span></span>



| <span data-ttu-id="61f99-119">Требование</span><span class="sxs-lookup"><span data-stu-id="61f99-119">Requirement</span></span> | <span data-ttu-id="61f99-120">Значение</span><span class="sxs-lookup"><span data-stu-id="61f99-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f99-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61f99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61f99-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61f99-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="61f99-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61f99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61f99-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61f99-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="61f99-125">DLL</span><span class="sxs-lookup"><span data-stu-id="61f99-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61f99-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61f99-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




