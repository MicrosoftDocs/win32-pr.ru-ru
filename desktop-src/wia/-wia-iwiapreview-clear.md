---
description: 'Освобождает нефильтрованное изображение, кэшированное методом Ивиапревиев:: Жетневпревиев. Он также освобождает фильтр обработки изображений.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Метод Ивиапревиев:: Clear (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701597"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="f923d-104">Метод Ивиапревиев:: Clear</span><span class="sxs-lookup"><span data-stu-id="f923d-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="f923d-105">Освобождает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="f923d-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="f923d-106">Он также освобождает фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="f923d-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f923d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f923d-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="f923d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f923d-108">Parameters</span></span>

<span data-ttu-id="f923d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f923d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f923d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f923d-110">Return value</span></span>

<span data-ttu-id="f923d-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f923d-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f923d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f923d-112">Remarks</span></span>

<span data-ttu-id="f923d-113">В **ивиапревиев:: Clear** компонент предварительной версии для получения образа Windows (WIA) 2,0 освобождает все хранящиеся в нем указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f923d-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="f923d-114">Компонент WIA 2,0 Preview сохраняет ссылки на *pWiaItem2* и *пвиатрансферкаллбакк* , переданные в [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="f923d-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="f923d-115">Чтобы быть точным, компонент WIA 2,0 Preview сохраняет ссылку на *pWiaItem2* и фильтр обработки изображений драйвера, который, в свою очередь, сохраняет ссылку на *пвиатрансферкаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="f923d-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="f923d-116">В **ивиапревиев:: Clear** компонент WIA 2,0 Preview также освобождает ссылку на *pWiaItem2* и на фильтр обработки изображений, который, в свою очередь, освобождает ссылку на *пвиатрансферкаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="f923d-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="f923d-117">Компонент WIA 2,0 Preview удаляет кэшированное нефильтрованное изображение, которое хранится внутри.</span><span class="sxs-lookup"><span data-stu-id="f923d-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="f923d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f923d-118">Requirements</span></span>



| <span data-ttu-id="f923d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f923d-119">Requirement</span></span> | <span data-ttu-id="f923d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f923d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f923d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f923d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f923d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f923d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f923d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f923d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f923d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f923d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f923d-125">Header</span><span class="sxs-lookup"><span data-stu-id="f923d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f923d-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f923d-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f923d-127">IDL</span><span class="sxs-lookup"><span data-stu-id="f923d-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f923d-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f923d-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




