---
description: Функция-посредник для метода Жетметадатакуеривритер.
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
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712697"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="adac5-103">Ивикфастметадатаенкодер \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="adac5-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="adac5-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="adac5-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adac5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adac5-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="adac5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adac5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adac5-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="adac5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adac5-108">Тип: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="adac5-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="adac5-109">Указатель на этот объект [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="adac5-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="adac5-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="adac5-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adac5-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="adac5-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="adac5-112">Указатель, получающий указатель на средство записи запросов метаданных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="adac5-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adac5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adac5-113">Return value</span></span>

<span data-ttu-id="adac5-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="adac5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="adac5-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="adac5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="adac5-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="adac5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="adac5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="adac5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="adac5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="adac5-118">Requirements</span></span>



| <span data-ttu-id="adac5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="adac5-119">Requirement</span></span> | <span data-ttu-id="adac5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="adac5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adac5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adac5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="adac5-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adac5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="adac5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adac5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="adac5-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="adac5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="adac5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="adac5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adac5-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adac5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




