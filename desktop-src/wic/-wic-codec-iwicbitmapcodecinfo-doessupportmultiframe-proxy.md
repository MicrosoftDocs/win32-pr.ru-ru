---
description: Функция-посредник для метода Доессуппортмултифраме.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: Функция IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144725"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="e7e52-103">ИвикбитмапкодеЦинфо \_ доессуппортмултифраме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e7e52-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="e7e52-104">Функция-посредник для метода [**доессуппортмултифраме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) .</span><span class="sxs-lookup"><span data-stu-id="e7e52-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e52-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e52-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="e7e52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e52-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="e7e52-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e52-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="e7e52-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="e7e52-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="e7e52-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="e7e52-110">*пфсуппортмултифраме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7e52-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e52-111">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="e7e52-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="e7e52-112">Указатель, получающий \*значение _ true\*\*, если кодек поддерживает изображения с несколькими кадрами; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e7e52-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e52-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7e52-113">Return value</span></span>

<span data-ttu-id="e7e52-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7e52-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e7e52-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e7e52-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7e52-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7e52-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e52-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7e52-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e52-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e52-118">Requirements</span></span>



| <span data-ttu-id="e7e52-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e52-119">Requirement</span></span> | <span data-ttu-id="e7e52-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e52-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e52-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7e52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e52-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7e52-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e7e52-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7e52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e52-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7e52-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e7e52-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e52-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e52-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7e52-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




