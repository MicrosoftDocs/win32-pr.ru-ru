---
description: Функция-посредник для метода Жетдевицемануфактурер.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: Функция IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710972"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="df74e-103">ИвикбитмапкодеЦинфо \_ жетдевицемануфактурер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="df74e-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="df74e-104">Функция-посредник для метода [**жетдевицемануфактурер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .</span><span class="sxs-lookup"><span data-stu-id="df74e-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="df74e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df74e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="df74e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df74e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df74e-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="df74e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df74e-108">Тип: \**[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="df74e-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="df74e-109">Указатель на этот объект [_ *ивикбитмапкодеЦинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="df74e-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="df74e-110">*кчдевицемануфактурер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df74e-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df74e-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="df74e-111">Type: **UINT**</span></span>

<span data-ttu-id="df74e-112">Размер названия производства устройства.</span><span class="sxs-lookup"><span data-stu-id="df74e-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="df74e-113">*вздевицемануфактурер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="df74e-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df74e-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="df74e-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="df74e-115">Указатель, получающий имя производителя устройства.</span><span class="sxs-lookup"><span data-stu-id="df74e-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="df74e-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="df74e-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df74e-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="df74e-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="df74e-118">Фактический размер буфера, необходимый для получения имени производителя устройства.</span><span class="sxs-lookup"><span data-stu-id="df74e-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df74e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df74e-119">Return value</span></span>

<span data-ttu-id="df74e-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="df74e-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="df74e-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="df74e-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df74e-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="df74e-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="df74e-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="df74e-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="df74e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="df74e-124">Requirements</span></span>



| <span data-ttu-id="df74e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="df74e-125">Requirement</span></span> | <span data-ttu-id="df74e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="df74e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df74e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df74e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df74e-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df74e-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="df74e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df74e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df74e-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df74e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="df74e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="df74e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df74e-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df74e-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




