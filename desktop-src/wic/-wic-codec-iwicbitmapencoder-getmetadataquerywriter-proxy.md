---
description: Функция-посредник для метода Жетметадатакуеривритер.
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
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692226"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="6a5d1-103">Ивикбитмапенкодер \_ жетметадатакуеривритер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="6a5d1-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="6a5d1-104">Функция-посредник для метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="6a5d1-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a5d1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="6a5d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a5d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5d1-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="6a5d1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5d1-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6a5d1-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="6a5d1-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="6a5d1-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6a5d1-110">*ппиметадатакуеривритер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6a5d1-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5d1-111">Тип: **[ **ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="6a5d1-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="6a5d1-112">Указатель, получающий указатель на [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="6a5d1-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a5d1-113">Return value</span></span>

<span data-ttu-id="6a5d1-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a5d1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6a5d1-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6a5d1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a5d1-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a5d1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5d1-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="6a5d1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5d1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6a5d1-118">Requirements</span></span>



| <span data-ttu-id="6a5d1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6a5d1-119">Requirement</span></span> | <span data-ttu-id="6a5d1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6a5d1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5d1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a5d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5d1-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a5d1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6a5d1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a5d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5d1-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a5d1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6a5d1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a5d1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a5d1-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a5d1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




