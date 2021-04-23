---
description: Функция-посредник для метода SetSize.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: Функция IWICBitmapFrameEncode_SetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693254"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="76a7a-103">Ивикбитмапфраминкоде \_ SetSize, \_ функция прокси</span><span class="sxs-lookup"><span data-stu-id="76a7a-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="76a7a-104">Функция-посредник для метода [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .</span><span class="sxs-lookup"><span data-stu-id="76a7a-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76a7a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="76a7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76a7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a7a-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="76a7a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a7a-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="76a7a-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="76a7a-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="76a7a-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="76a7a-110">*уивидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76a7a-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a7a-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="76a7a-111">Type: **UINT**</span></span>

<span data-ttu-id="76a7a-112">Ширина выходного изображения.</span><span class="sxs-lookup"><span data-stu-id="76a7a-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="76a7a-113">*уихеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76a7a-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a7a-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="76a7a-114">Type: **UINT**</span></span>

<span data-ttu-id="76a7a-115">Высота выходного изображения.</span><span class="sxs-lookup"><span data-stu-id="76a7a-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a7a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76a7a-116">Return value</span></span>

<span data-ttu-id="76a7a-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="76a7a-117">Type: **HRESULT**</span></span>

<span data-ttu-id="76a7a-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="76a7a-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76a7a-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76a7a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76a7a-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="76a7a-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="76a7a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="76a7a-121">Requirements</span></span>



| <span data-ttu-id="76a7a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="76a7a-122">Requirement</span></span> | <span data-ttu-id="76a7a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="76a7a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a7a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76a7a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76a7a-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76a7a-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="76a7a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76a7a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76a7a-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76a7a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="76a7a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="76a7a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76a7a-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76a7a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




