---
description: Функция-посредник для метода Жетмиметипес.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: Функция IWICBitmapCodecInfo_GetMimeTypes_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541271"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="18b42-103">ИвикбитмапкодеЦинфо \_ жетмиметипес \_ -функция</span><span class="sxs-lookup"><span data-stu-id="18b42-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="18b42-104">Функция-посредник для метода [**жетмиметипес**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .</span><span class="sxs-lookup"><span data-stu-id="18b42-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b42-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18b42-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="18b42-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18b42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b42-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="18b42-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b42-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="18b42-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="18b42-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="18b42-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="18b42-110">*кчмиметипес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b42-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b42-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="18b42-111">Type: **UINT**</span></span>

<span data-ttu-id="18b42-112">Размер буфера типов MIME.</span><span class="sxs-lookup"><span data-stu-id="18b42-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="18b42-113">*взмиметипес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18b42-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18b42-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="18b42-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="18b42-115">Указатель, получающий типы MIME, связанные с кодеком.</span><span class="sxs-lookup"><span data-stu-id="18b42-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="18b42-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18b42-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18b42-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="18b42-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="18b42-118">Фактический размер буфера, необходимый для получения всех типов MIME, связанных с кодеком.</span><span class="sxs-lookup"><span data-stu-id="18b42-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b42-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18b42-119">Return value</span></span>

<span data-ttu-id="18b42-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="18b42-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="18b42-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="18b42-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18b42-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18b42-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b42-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="18b42-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="18b42-124">Требования</span><span class="sxs-lookup"><span data-stu-id="18b42-124">Requirements</span></span>



| <span data-ttu-id="18b42-125">Требование</span><span class="sxs-lookup"><span data-stu-id="18b42-125">Requirement</span></span> | <span data-ttu-id="18b42-126">Значение</span><span class="sxs-lookup"><span data-stu-id="18b42-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b42-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18b42-127">Minimum supported client</span></span><br/> | <span data-ttu-id="18b42-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18b42-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="18b42-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18b42-129">Minimum supported server</span></span><br/> | <span data-ttu-id="18b42-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18b42-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="18b42-131">DLL</span><span class="sxs-lookup"><span data-stu-id="18b42-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b42-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18b42-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




