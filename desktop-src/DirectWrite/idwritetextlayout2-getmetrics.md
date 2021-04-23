---
title: Метод IDWriteTextLayout2ических метрик
description: Получает общие метрики для форматированной строки.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Прямая запись методаических метрик
- Интерфейс IDWriteTextLayout2 с прямым написанием с методомических метрик
- Интерфейс IDWriteTextLayout2 Direct Write, методических метрик
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681952"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="6237b-106">Метод IDWriteTextLayout2:: с метриками</span><span class="sxs-lookup"><span data-stu-id="6237b-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="6237b-107">Получает общие метрики для форматированной строки.</span><span class="sxs-lookup"><span data-stu-id="6237b-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6237b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6237b-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6237b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6237b-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="6237b-110">*текстметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6237b-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6237b-111">Введите: \**[**дврите \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="6237b-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="6237b-112">При возврате из этого метода содержит измеряемое расстояние текста и связанного содержимого после форматирования.</span><span class="sxs-lookup"><span data-stu-id="6237b-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6237b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6237b-113">Return value</span></span>

<span data-ttu-id="6237b-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6237b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6237b-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6237b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6237b-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6237b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6237b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6237b-117">Requirements</span></span>



| <span data-ttu-id="6237b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6237b-118">Requirement</span></span> | <span data-ttu-id="6237b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6237b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6237b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6237b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6237b-121">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="6237b-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6237b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6237b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6237b-123">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6237b-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6237b-124">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="6237b-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6237b-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="6237b-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="6237b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6237b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6237b-127"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6237b-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6237b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6237b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6237b-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6237b-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6237b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6237b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6237b-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="6237b-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





