---
description: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy функция-прокси для метода Жетметадатакуеривритер.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: Функция IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091172"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="19b63-103">Ивикбитмапенкодер \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="19b63-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="19b63-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="19b63-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19b63-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="19b63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19b63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b63-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="19b63-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b63-108">Тип: **[ **ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="19b63-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="19b63-109">Указатель на этот объект [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="19b63-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="19b63-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="19b63-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19b63-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="19b63-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="19b63-112">Указатель, получающий указатель на [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="19b63-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b63-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19b63-113">Return value</span></span>

<span data-ttu-id="19b63-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19b63-114">Type: **HRESULT**</span></span>

<span data-ttu-id="19b63-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="19b63-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19b63-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19b63-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19b63-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="19b63-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="19b63-118">Требования</span><span class="sxs-lookup"><span data-stu-id="19b63-118">Requirements</span></span>



| <span data-ttu-id="19b63-119">Требование</span><span class="sxs-lookup"><span data-stu-id="19b63-119">Requirement</span></span> | <span data-ttu-id="19b63-120">Значение</span><span class="sxs-lookup"><span data-stu-id="19b63-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b63-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19b63-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19b63-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19b63-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="19b63-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19b63-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19b63-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19b63-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="19b63-125">DLL</span><span class="sxs-lookup"><span data-stu-id="19b63-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b63-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19b63-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




