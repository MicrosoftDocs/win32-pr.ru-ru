---
description: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy функция-прокси для метода Жетметадатакуеривритер.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: Функция IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113612"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="29df6-103">Ивикбитмапфраминкоде \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="29df6-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="29df6-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="29df6-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29df6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29df6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="29df6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29df6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29df6-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="29df6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29df6-108">Тип: **[ **ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="29df6-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="29df6-109">Указатель на этот объект [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="29df6-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="29df6-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="29df6-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29df6-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="29df6-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="29df6-112">Указатель, получающий средство записи запросов метаданных для кадра.</span><span class="sxs-lookup"><span data-stu-id="29df6-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29df6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29df6-113">Return value</span></span>

<span data-ttu-id="29df6-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29df6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="29df6-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="29df6-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29df6-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29df6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29df6-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="29df6-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="29df6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="29df6-118">Requirements</span></span>



| <span data-ttu-id="29df6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="29df6-119">Requirement</span></span> | <span data-ttu-id="29df6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="29df6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29df6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29df6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29df6-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29df6-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="29df6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29df6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29df6-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29df6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="29df6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="29df6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29df6-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29df6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




