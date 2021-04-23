---
description: Функция-посредник для метода Жетенкодеринфо.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: Функция IWICBitmapEncoder_GetEncoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693762"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="e49c5-103">Ивикбитмапенкодер \_ жетенкодеринфо \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e49c5-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="e49c5-104">Функция-посредник для метода [**жетенкодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="e49c5-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e49c5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e49c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e49c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49c5-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="e49c5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49c5-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="e49c5-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="e49c5-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="e49c5-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="e49c5-110">*ппиенкодеринфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e49c5-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e49c5-111">Тип: **[ **ивикбитмапенкодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="e49c5-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="e49c5-112">Указатель, получающий указатель на [**ивикбитмапенкодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span><span class="sxs-lookup"><span data-stu-id="e49c5-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49c5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e49c5-113">Return value</span></span>

<span data-ttu-id="e49c5-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e49c5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e49c5-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e49c5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e49c5-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e49c5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49c5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="e49c5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e49c5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e49c5-118">Requirements</span></span>



| <span data-ttu-id="e49c5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e49c5-119">Requirement</span></span> | <span data-ttu-id="e49c5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e49c5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e49c5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e49c5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e49c5-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e49c5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e49c5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e49c5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e49c5-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e49c5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e49c5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e49c5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49c5-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e49c5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




