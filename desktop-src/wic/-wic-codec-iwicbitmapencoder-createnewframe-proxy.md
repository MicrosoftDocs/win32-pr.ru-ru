---
description: Функция-посредник для метода CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: Функция IWICBitmapEncoder_CreateNewFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693456"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="85e67-103">Ивикбитмапенкодер \_ CreateNewFrame \_ -функция</span><span class="sxs-lookup"><span data-stu-id="85e67-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="85e67-104">Функция-посредник для метода [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .</span><span class="sxs-lookup"><span data-stu-id="85e67-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85e67-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="85e67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85e67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e67-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="85e67-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e67-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="85e67-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="85e67-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="85e67-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="85e67-110">*ппифраминкоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85e67-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e67-111">Тип: **[ **ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="85e67-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="85e67-112">Указатель, получающий указатель на новый экземпляр объекта [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="85e67-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="85e67-113">*ппиенкодероптионс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="85e67-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e67-114">Тип: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="85e67-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="85e67-115">Именованные свойства, используемые для инициализации кадра.</span><span class="sxs-lookup"><span data-stu-id="85e67-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e67-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85e67-116">Return value</span></span>

<span data-ttu-id="85e67-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85e67-117">Type: **HRESULT**</span></span>

<span data-ttu-id="85e67-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85e67-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85e67-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85e67-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e67-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="85e67-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="85e67-121">Требования</span><span class="sxs-lookup"><span data-stu-id="85e67-121">Requirements</span></span>



| <span data-ttu-id="85e67-122">Требование</span><span class="sxs-lookup"><span data-stu-id="85e67-122">Requirement</span></span> | <span data-ttu-id="85e67-123">Значение</span><span class="sxs-lookup"><span data-stu-id="85e67-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e67-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85e67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85e67-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85e67-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="85e67-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85e67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85e67-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85e67-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="85e67-128">DLL</span><span class="sxs-lookup"><span data-stu-id="85e67-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85e67-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85e67-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

