---
description: Функция-посредник для метода Жетметадатакуериреадер.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: Функция IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701440"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="b9101-103">IWICBitmapFrameDecode \_ жетметадатакуериреадер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="b9101-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="b9101-104">Функция-посредник для метода [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="b9101-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9101-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9101-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="b9101-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9101-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="b9101-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9101-108">Тип: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="b9101-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="b9101-109">Указатель на этот объект [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="b9101-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b9101-110">*ппиметадатакуериреадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b9101-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9101-111">Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="b9101-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="b9101-112">Указатель, получающий указатель на [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="b9101-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9101-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9101-113">Return value</span></span>

<span data-ttu-id="b9101-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9101-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b9101-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b9101-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9101-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9101-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9101-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="b9101-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b9101-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b9101-118">Requirements</span></span>



| <span data-ttu-id="b9101-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b9101-119">Requirement</span></span> | <span data-ttu-id="b9101-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b9101-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9101-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9101-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9101-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9101-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b9101-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9101-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9101-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9101-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b9101-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9101-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9101-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9101-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




