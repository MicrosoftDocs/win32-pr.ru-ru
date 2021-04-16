---
description: Функция-посредник для метода OnPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: Функция IWICBitmapDecoder_GetPreview_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692227"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="2980d-103">\_ \_ Функция прокси Ивикбитмапдекодер-Preview</span><span class="sxs-lookup"><span data-stu-id="2980d-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="2980d-104">Функция-посредник для метода [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="2980d-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2980d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2980d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="2980d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2980d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2980d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="2980d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2980d-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="2980d-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="2980d-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="2980d-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="2980d-110">*ппибитмапсаурце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2980d-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2980d-111">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="2980d-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="2980d-112">Указатель, получающий указатель на битовую карту предварительного просмотра, если поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2980d-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2980d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2980d-113">Return value</span></span>

<span data-ttu-id="2980d-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2980d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2980d-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2980d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2980d-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2980d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2980d-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="2980d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2980d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2980d-118">Requirements</span></span>



| <span data-ttu-id="2980d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2980d-119">Requirement</span></span> | <span data-ttu-id="2980d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2980d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2980d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2980d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2980d-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2980d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2980d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2980d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2980d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2980d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2980d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2980d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2980d-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2980d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




