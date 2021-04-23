---
description: Функция-посредник для метода Жетфиликстенсионс.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: Функция IWICBitmapCodecInfo_GetFileExtensions_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343232"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="0f318-103">ИвикбитмапкодеЦинфо \_ жетфиликстенсионс \_ -функция</span><span class="sxs-lookup"><span data-stu-id="0f318-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="0f318-104">Функция-посредник для метода [**жетфиликстенсионс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .</span><span class="sxs-lookup"><span data-stu-id="0f318-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f318-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f318-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="0f318-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f318-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="0f318-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f318-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="0f318-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="0f318-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="0f318-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="0f318-110">*кчфиликстенсионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f318-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f318-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="0f318-111">Type: **UINT**</span></span>

<span data-ttu-id="0f318-112">Размер буфера расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="0f318-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0f318-113">*взфиликстенсионс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0f318-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f318-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0f318-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="0f318-115">Указатель, получающий расширения имен файлов, связанные с кодеком.</span><span class="sxs-lookup"><span data-stu-id="0f318-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="0f318-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f318-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f318-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="0f318-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="0f318-118">Фактический размер буфера, необходимый для получения всех расширений имен файлов, связанных с кодеком.</span><span class="sxs-lookup"><span data-stu-id="0f318-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f318-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f318-119">Return value</span></span>

<span data-ttu-id="0f318-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0f318-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0f318-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0f318-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f318-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f318-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f318-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="0f318-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0f318-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0f318-124">Requirements</span></span>



| <span data-ttu-id="0f318-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0f318-125">Requirement</span></span> | <span data-ttu-id="0f318-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0f318-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f318-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f318-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0f318-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f318-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0f318-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f318-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0f318-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f318-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0f318-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0f318-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f318-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f318-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




