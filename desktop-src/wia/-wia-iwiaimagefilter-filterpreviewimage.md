---
description: Фильтрует изображение предварительного просмотра.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Метод Ивиаимажефилтер:: Филтерпревиевимаже (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711250"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="bcc2d-103">Метод Ивиаимажефилтер:: Филтерпревиевимаже</span><span class="sxs-lookup"><span data-stu-id="bcc2d-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="bcc2d-104">Фильтрует изображение предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcc2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcc2d-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="bcc2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcc2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc2d-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc2d-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="bcc2d-108">Type: **LONG**</span></span>

<span data-ttu-id="bcc2d-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-109">Not used.</span></span> <span data-ttu-id="bcc2d-110">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="bcc2d-111">*pWiaChildItem2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc2d-112">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="bcc2d-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="bcc2d-113">Обрабатываемый элемент.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="bcc2d-114">_InputImageExtents \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc2d-115">Тип: **Rect**</span><span class="sxs-lookup"><span data-stu-id="bcc2d-115">Type: **RECT**</span></span>

<span data-ttu-id="bcc2d-116">Координаты (в области физического приобретения) образа, который компонент предварительной версии кэширует внутренне.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="bcc2d-117">*пинпутстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc2d-118">Тип: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="bcc2d-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="bcc2d-119">Указатель на интерфейс [IStream](/windows/win32/api/objidl/nn-objidl-istream) для фильтруемых данных изображения в кэше.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc2d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcc2d-120">Return value</span></span>

<span data-ttu-id="bcc2d-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="bcc2d-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="bcc2d-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bcc2d-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bcc2d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc2d-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcc2d-124">Remarks</span></span>

<span data-ttu-id="bcc2d-125">Не вызывайте этот метод непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="bcc2d-126">*pWiaChildItem2* должен быть дочерним элементом *pWiaItem2* , переданным в [**ивиаимажефилтер:: инитиализефилтер**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="bcc2d-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="bcc2d-127">*Инпутимажеекстентс* требуется, поскольку фильтр обработки изображений отвечает за Вырезание области изображения, которую *pWiaChildItem2* представляет из данных изображения, передаваемых через *пинпутстреам*.</span><span class="sxs-lookup"><span data-stu-id="bcc2d-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="bcc2d-128">Приложение должно гарантировать, что *pWiaChildItem2* имеет тот же формат изображения ( \_ Формат WIA IPA \_ ), разрешение (с помощью WIA-пакетов \_ \_ ксрес и WIA \_ \_ -адресов ИРЕС) и глубину ( \_ глубину WIA IPA \_ ) в качестве *pWiaItem2* при передаче в [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="bcc2d-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc2d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bcc2d-129">Requirements</span></span>



| <span data-ttu-id="bcc2d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="bcc2d-130">Requirement</span></span> | <span data-ttu-id="bcc2d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bcc2d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc2d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcc2d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc2d-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bcc2d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcc2d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc2d-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bcc2d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bcc2d-136">Header</span><span class="sxs-lookup"><span data-stu-id="bcc2d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc2d-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc2d-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="bcc2d-138">IDL</span><span class="sxs-lookup"><span data-stu-id="bcc2d-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bcc2d-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bcc2d-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
