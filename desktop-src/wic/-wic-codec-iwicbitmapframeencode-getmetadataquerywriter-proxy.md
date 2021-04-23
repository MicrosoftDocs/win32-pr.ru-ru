---
description: Функция-посредник для метода Жетметадатакуеривритер.
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
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809568"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="f0a96-103">Ивикбитмапфраминкоде \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="f0a96-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="f0a96-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="f0a96-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0a96-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="f0a96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a96-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="f0a96-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a96-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="f0a96-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="f0a96-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="f0a96-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="f0a96-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0a96-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a96-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0a96-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="f0a96-112">Указатель, получающий средство записи запросов метаданных для кадра.</span><span class="sxs-lookup"><span data-stu-id="f0a96-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a96-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0a96-113">Return value</span></span>

<span data-ttu-id="f0a96-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0a96-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f0a96-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0a96-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0a96-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0a96-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a96-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="f0a96-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a96-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f0a96-118">Requirements</span></span>



| <span data-ttu-id="f0a96-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f0a96-119">Requirement</span></span> | <span data-ttu-id="f0a96-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f0a96-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a96-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0a96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a96-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0a96-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f0a96-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0a96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a96-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0a96-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f0a96-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a96-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a96-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0a96-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




