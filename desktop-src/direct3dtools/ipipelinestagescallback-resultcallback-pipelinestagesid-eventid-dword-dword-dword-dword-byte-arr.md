---
description: Обратный вызов, уведомляющий узел о том, что данные образа этапа конвейера возвращены запросом связана.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342045"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="12633-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>Метод Ипипелинестажескаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="12633-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="12633-104">Обратный вызов, уведомляющий узел о том, что данные образа этапа конвейера возвращены запросом связана.</span><span class="sxs-lookup"><span data-stu-id="12633-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="12633-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12633-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="12633-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12633-106">Parameters</span></span>

<span data-ttu-id="12633-107">*стажеид* </span><span class="sxs-lookup"><span data-stu-id="12633-107">*stageId* </span></span>  
<span data-ttu-id="12633-108">Этап конвейера, представленный в результатах.</span><span class="sxs-lookup"><span data-stu-id="12633-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="12633-109">*Аль* </span><span class="sxs-lookup"><span data-stu-id="12633-109">*eid* </span></span>  
<span data-ttu-id="12633-110">Событие, представленное в результатах.</span><span class="sxs-lookup"><span data-stu-id="12633-110">The event represented in the results.</span></span>

<span data-ttu-id="12633-111">*Ширина* </span><span class="sxs-lookup"><span data-stu-id="12633-111">*width* </span></span>  
<span data-ttu-id="12633-112">Ширина образа визуализации конвейера.</span><span class="sxs-lookup"><span data-stu-id="12633-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="12633-113">*равно* </span><span class="sxs-lookup"><span data-stu-id="12633-113">*height* </span></span>  
<span data-ttu-id="12633-114">Высота изображения визуализации конвейера.</span><span class="sxs-lookup"><span data-stu-id="12633-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="12633-115">*формат* </span><span class="sxs-lookup"><span data-stu-id="12633-115">*format* </span></span>  
<span data-ttu-id="12633-116">Формат образа визуализации конвейера.</span><span class="sxs-lookup"><span data-stu-id="12633-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="12633-117">*изменять* </span><span class="sxs-lookup"><span data-stu-id="12633-117">*size* </span></span>  
<span data-ttu-id="12633-118">Размер изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="12633-118">The size of the image in bytes.</span></span>

<span data-ttu-id="12633-119">*\_буфер count5* </span><span class="sxs-lookup"><span data-stu-id="12633-119">*count5\_buffer* </span></span>  
<span data-ttu-id="12633-120">Образ визуализации конвейера.</span><span class="sxs-lookup"><span data-stu-id="12633-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="12633-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12633-121">Return value</span></span>

<span data-ttu-id="12633-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="12633-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12633-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12633-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12633-124">Требования</span><span class="sxs-lookup"><span data-stu-id="12633-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="12633-125">Header</span><span class="sxs-lookup"><span data-stu-id="12633-125">Header</span></span></p></td><td><span data-ttu-id="12633-126">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="12633-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="12633-127"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="12633-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="12633-128">**ипипелинестажескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="12633-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
