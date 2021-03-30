---
description: Функция-посредник для метода CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: Функция IWICBitmapSource_CopyPixels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266146"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="11d49-103">IWICBitmapSource \_ CopyPixels \_ -функция</span><span class="sxs-lookup"><span data-stu-id="11d49-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="11d49-104">Функция-посредник для метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="11d49-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11d49-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="11d49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11d49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d49-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="11d49-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d49-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="11d49-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="11d49-109">Указатель на этот объект [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="11d49-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="11d49-110">*КНР* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11d49-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d49-111">Тип: \**const [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="11d49-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="11d49-112">Копируемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="11d49-112">The rectangle to copy.</span></span> <span data-ttu-id="11d49-113">Значение NULL указывает всю битовую карту.</span><span class="sxs-lookup"><span data-stu-id="11d49-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="11d49-114">_cbStride \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="11d49-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d49-115">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="11d49-115">Type: **UINT**</span></span>

<span data-ttu-id="11d49-116">Шаг точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="11d49-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="11d49-117">*кббуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11d49-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d49-118">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="11d49-118">Type: **UINT**</span></span>

<span data-ttu-id="11d49-119">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="11d49-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="11d49-120">*пббуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11d49-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11d49-121">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="11d49-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="11d49-122">Указатель на буфер.</span><span class="sxs-lookup"><span data-stu-id="11d49-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11d49-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11d49-123">Return value</span></span>

<span data-ttu-id="11d49-124">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="11d49-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="11d49-125">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="11d49-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11d49-126">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11d49-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11d49-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="11d49-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="11d49-128">Требования</span><span class="sxs-lookup"><span data-stu-id="11d49-128">Requirements</span></span>



| <span data-ttu-id="11d49-129">Требование</span><span class="sxs-lookup"><span data-stu-id="11d49-129">Requirement</span></span> | <span data-ttu-id="11d49-130">Значение</span><span class="sxs-lookup"><span data-stu-id="11d49-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d49-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11d49-131">Minimum supported client</span></span><br/> | <span data-ttu-id="11d49-132">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11d49-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="11d49-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11d49-133">Minimum supported server</span></span><br/> | <span data-ttu-id="11d49-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11d49-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="11d49-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11d49-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d49-136"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11d49-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




