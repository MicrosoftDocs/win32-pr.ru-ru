---
description: Функция-посредник для метода Сетсумбнаил.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: Функция IWICBitmapFrameEncode_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911387"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="5aa4d-103">Ивикбитмапфраминкоде \_ сетсумбнаил \_ -функция</span><span class="sxs-lookup"><span data-stu-id="5aa4d-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="5aa4d-104">Функция-посредник для метода [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="5aa4d-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aa4d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="5aa4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aa4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa4d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="5aa4d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa4d-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="5aa4d-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="5aa4d-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="5aa4d-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="5aa4d-110">*писумбнаил* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aa4d-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa4d-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="5aa4d-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="5aa4d-112">Источник точечного рисунка для использования в качестве эскиза.</span><span class="sxs-lookup"><span data-stu-id="5aa4d-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa4d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aa4d-113">Return value</span></span>

<span data-ttu-id="5aa4d-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5aa4d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5aa4d-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5aa4d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aa4d-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5aa4d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa4d-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="5aa4d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa4d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5aa4d-118">Requirements</span></span>



| <span data-ttu-id="5aa4d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5aa4d-119">Requirement</span></span> | <span data-ttu-id="5aa4d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa4d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa4d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5aa4d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa4d-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5aa4d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5aa4d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5aa4d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa4d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5aa4d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5aa4d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5aa4d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa4d-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aa4d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




