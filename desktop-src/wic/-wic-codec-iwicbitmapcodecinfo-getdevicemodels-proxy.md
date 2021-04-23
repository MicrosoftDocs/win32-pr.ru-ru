---
description: Функция-посредник для метода Жетдевицемоделс.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: Функция IWICBitmapCodecInfo_GetDeviceModels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710971"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="9b41c-103">ИвикбитмапкодеЦинфо \_ жетдевицемоделс \_ -функция</span><span class="sxs-lookup"><span data-stu-id="9b41c-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="9b41c-104">Функция-посредник для метода [**жетдевицемоделс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .</span><span class="sxs-lookup"><span data-stu-id="9b41c-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b41c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b41c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="9b41c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b41c-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b41c-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9b41c-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="9b41c-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="9b41c-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9b41c-110">*кчдевицемоделс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b41c-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b41c-111">Type: **UINT**</span></span>

<span data-ttu-id="9b41c-112">Размер буфера моделей устройств.</span><span class="sxs-lookup"><span data-stu-id="9b41c-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9b41c-113">*вздевицемоделс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b41c-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9b41c-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9b41c-115">Указатель, получающий разделенный запятыми список имен моделей устройств, связанных с кодеком.</span><span class="sxs-lookup"><span data-stu-id="9b41c-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="9b41c-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b41c-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9b41c-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="9b41c-118">Фактический размер буфера, необходимый для получения всех имен моделей устройств.</span><span class="sxs-lookup"><span data-stu-id="9b41c-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b41c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b41c-119">Return value</span></span>

<span data-ttu-id="9b41c-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9b41c-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9b41c-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b41c-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b41c-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b41c-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b41c-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b41c-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9b41c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9b41c-124">Requirements</span></span>



| <span data-ttu-id="9b41c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9b41c-125">Requirement</span></span> | <span data-ttu-id="9b41c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9b41c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b41c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b41c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b41c-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9b41c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b41c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b41c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b41c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9b41c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9b41c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b41c-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b41c-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




