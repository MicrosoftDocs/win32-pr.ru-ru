---
description: Функция-посредник для метода Initialize.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: Функция IWICBitmapFrameEncode_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809563"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="51780-103">Ивикбитмапфраминкоде \_ инициализировать \_ прокси-функцию</span><span class="sxs-lookup"><span data-stu-id="51780-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="51780-104">Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="51780-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51780-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51780-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="51780-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51780-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="51780-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51780-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="51780-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="51780-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="51780-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="51780-110">*пиенкодероптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51780-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51780-111">Тип: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="51780-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="51780-112">Набор свойств, используемых для инициализации [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="51780-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51780-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51780-113">Return value</span></span>

<span data-ttu-id="51780-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="51780-114">Type: **HRESULT**</span></span>

<span data-ttu-id="51780-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="51780-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51780-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51780-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51780-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="51780-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="51780-118">Требования</span><span class="sxs-lookup"><span data-stu-id="51780-118">Requirements</span></span>



| <span data-ttu-id="51780-119">Требование</span><span class="sxs-lookup"><span data-stu-id="51780-119">Requirement</span></span> | <span data-ttu-id="51780-120">Значение</span><span class="sxs-lookup"><span data-stu-id="51780-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51780-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51780-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51780-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51780-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="51780-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51780-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51780-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51780-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="51780-125">DLL</span><span class="sxs-lookup"><span data-stu-id="51780-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51780-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51780-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

