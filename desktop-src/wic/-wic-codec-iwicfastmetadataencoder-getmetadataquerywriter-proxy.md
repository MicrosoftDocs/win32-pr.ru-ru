---
description: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy функция-прокси для метода Жетметадатакуеривритер.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: Функция IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097172"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="cf05e-103">Ивикфастметадатаенкодер \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="cf05e-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="cf05e-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="cf05e-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf05e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf05e-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="cf05e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf05e-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="cf05e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf05e-108">Тип: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="cf05e-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="cf05e-109">Указатель на этот объект [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="cf05e-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="cf05e-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf05e-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf05e-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="cf05e-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="cf05e-112">Указатель, получающий указатель на средство записи запросов метаданных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cf05e-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf05e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf05e-113">Return value</span></span>

<span data-ttu-id="cf05e-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cf05e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cf05e-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cf05e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf05e-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf05e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf05e-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="cf05e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cf05e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cf05e-118">Requirements</span></span>



| <span data-ttu-id="cf05e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cf05e-119">Requirement</span></span> | <span data-ttu-id="cf05e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf05e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf05e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf05e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf05e-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf05e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cf05e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf05e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf05e-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf05e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cf05e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cf05e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf05e-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf05e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




