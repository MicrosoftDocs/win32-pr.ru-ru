---
description: Запросы на запуск автономного анализа с указанным источником, манифестом, параметрами и указанным кадром.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисисрекуест:: Рекуестоффлинеаналисисасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422953"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="9d80e-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Метод Иоффлинеаналисисрекуест:: Рекуестоффлинеаналисисасинк</span><span class="sxs-lookup"><span data-stu-id="9d80e-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="9d80e-104">Запросы на запуск автономного анализа с указанным источником, манифестом, параметрами и указанным кадром.</span><span class="sxs-lookup"><span data-stu-id="9d80e-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d80e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d80e-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="9d80e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d80e-106">Parameters</span></span>

<span data-ttu-id="9d80e-107">*аналисиссаурце* </span><span class="sxs-lookup"><span data-stu-id="9d80e-107">*analysisSource* </span></span>  
<span data-ttu-id="9d80e-108">Спекфиес, где источник анализа получен из кэшированных отчетов или из воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9d80e-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="9d80e-109">*манифестксмл* </span><span class="sxs-lookup"><span data-stu-id="9d80e-109">*manifestXml* </span></span>  
<span data-ttu-id="9d80e-110">Строка COM, содержащая путь к XML-файлу манифеста.</span><span class="sxs-lookup"><span data-stu-id="9d80e-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="9d80e-111">*параметерсксмл* </span><span class="sxs-lookup"><span data-stu-id="9d80e-111">*parametersXml* </span></span>  
<span data-ttu-id="9d80e-112">Строка COM, содержащая путь к XML-файлу параметров.</span><span class="sxs-lookup"><span data-stu-id="9d80e-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="9d80e-113">*"* </span><span class="sxs-lookup"><span data-stu-id="9d80e-113">*cookie* </span></span>  
<span data-ttu-id="9d80e-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="9d80e-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="9d80e-115">*каптурефуллфиленаме* </span><span class="sxs-lookup"><span data-stu-id="9d80e-115">*captureFullFileName* </span></span>  
<span data-ttu-id="9d80e-116">Строка COM, содержащая абсолютный путь к файлу записи (. vsglog).</span><span class="sxs-lookup"><span data-stu-id="9d80e-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="9d80e-117">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="9d80e-117">*frameNumber* </span></span>  
<span data-ttu-id="9d80e-118">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="9d80e-118">The specified frame.</span></span>

<span data-ttu-id="9d80e-119">*аутпутфуллфиленаме* </span><span class="sxs-lookup"><span data-stu-id="9d80e-119">*outputFullFileName* </span></span>  
<span data-ttu-id="9d80e-120">Строка COM, содержащая абсолютный путь к файлу, в который записываются выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9d80e-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="9d80e-121">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="9d80e-121">*requestCallback* </span></span>  
<span data-ttu-id="9d80e-122">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="9d80e-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d80e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d80e-123">Return value</span></span>

<span data-ttu-id="9d80e-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9d80e-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d80e-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d80e-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d80e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9d80e-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9d80e-127">Header</span><span class="sxs-lookup"><span data-stu-id="9d80e-127">Header</span></span></p></td><td><span data-ttu-id="9d80e-128">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="9d80e-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9d80e-129"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="9d80e-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9d80e-130">**иоффлинеаналисисрекуест**</span><span class="sxs-lookup"><span data-stu-id="9d80e-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
