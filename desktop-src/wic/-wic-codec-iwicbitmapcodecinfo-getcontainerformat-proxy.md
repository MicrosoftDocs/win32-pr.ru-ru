---
description: Функция-посредник для метода Жетконтаинерформат.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: Функция IWICBitmapCodecInfo_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263027"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="f0fc7-103">ИвикбитмапкодеЦинфо \_ жетконтаинерформат \_ -функция</span><span class="sxs-lookup"><span data-stu-id="f0fc7-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="f0fc7-104">Функция-посредник для метода [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="f0fc7-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fc7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0fc7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f0fc7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0fc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0fc7-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="f0fc7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fc7-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f0fc7-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="f0fc7-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="f0fc7-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="f0fc7-110">*пгуидконтаинерформат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0fc7-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fc7-111">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f0fc7-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="f0fc7-112">Указатель, получающий идентификатор GUID контейнера.</span><span class="sxs-lookup"><span data-stu-id="f0fc7-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0fc7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0fc7-113">Return value</span></span>

<span data-ttu-id="f0fc7-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f0fc7-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f0fc7-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0fc7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0fc7-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0fc7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0fc7-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="f0fc7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f0fc7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f0fc7-118">Requirements</span></span>



| <span data-ttu-id="f0fc7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f0fc7-119">Requirement</span></span> | <span data-ttu-id="f0fc7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f0fc7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fc7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0fc7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0fc7-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0fc7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f0fc7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0fc7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0fc7-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0fc7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f0fc7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0fc7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0fc7-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




