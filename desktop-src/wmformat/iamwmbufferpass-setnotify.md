---
title: Иамвмбуфферпасс Сетнотифи, метод
description: Метод Сетнотифи используется приложениями для предоставления модулю записи WM ASF или фильтра чтения WM ASF указателя на интерфейс Иамвмбуфферпасскаллбакк приложения.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Формат Windows Media, Сетнотифи метод
- Сетнотифи метод Windows Media Format, интерфейс Иамвмбуфферпасс
- Интерфейс Иамвмбуфферпасс Windows Media Format, метод Сетнотифи
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413495"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="5d61b-106">Метод Иамвмбуфферпасс:: Сетнотифи</span><span class="sxs-lookup"><span data-stu-id="5d61b-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="5d61b-107">Метод **сетнотифи** используется приложениями для предоставления модулю записи WM ASF или фильтра [чтения WM ASF](wm-asf-reader-filter.md) указателя на интерфейс [**иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) приложения.</span><span class="sxs-lookup"><span data-stu-id="5d61b-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d61b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d61b-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="5d61b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d61b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d61b-110">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d61b-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d61b-111">Указатель на интерфейс **иамвмбуфферпасскаллбакк** приложения.</span><span class="sxs-lookup"><span data-stu-id="5d61b-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d61b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d61b-112">Return value</span></span>

<span data-ttu-id="5d61b-113">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5d61b-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5d61b-114">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d61b-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d61b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d61b-115">Remarks</span></span>

<span data-ttu-id="5d61b-116">Вызовите этот метод перед переводом графа фильтра в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d61b-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d61b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d61b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d61b-118">**Интерфейс Иамвмбуфферпасс**</span><span class="sxs-lookup"><span data-stu-id="5d61b-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 