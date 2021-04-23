---
description: Функция обратного вызова, используемая для уведомления узла о завершении автономного анализа.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисискаллбакк:: Оффлинеаналисискомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538204"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="790c8-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Метод Иоффлинеаналисискаллбакк:: Оффлинеаналисискомплете</span><span class="sxs-lookup"><span data-stu-id="790c8-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="790c8-104">Функция обратного вызова, используемая для уведомления узла о завершении автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="790c8-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="790c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="790c8-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="790c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="790c8-106">Parameters</span></span>

<span data-ttu-id="790c8-107">*"* </span><span class="sxs-lookup"><span data-stu-id="790c8-107">*cookie* </span></span>  
<span data-ttu-id="790c8-108">Файл cookie, который однозначно определяет запрос, который инициировал анализ в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="790c8-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="790c8-109">*результат* </span><span class="sxs-lookup"><span data-stu-id="790c8-109">*result* </span></span>  
<span data-ttu-id="790c8-110">Указывает, завершился ли автономный анализ успешно или нет.</span><span class="sxs-lookup"><span data-stu-id="790c8-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="790c8-111">В случае успеха результаты были записаны в файл.</span><span class="sxs-lookup"><span data-stu-id="790c8-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="790c8-112">*аутпутфуллфиленаме* </span><span class="sxs-lookup"><span data-stu-id="790c8-112">*outputFullFileName* </span></span>  
<span data-ttu-id="790c8-113">Строка COM, контианинг имя файла, в котором были записаны результаты автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="790c8-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="790c8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="790c8-114">Return value</span></span>

<span data-ttu-id="790c8-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="790c8-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="790c8-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="790c8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="790c8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="790c8-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="790c8-118">Header</span><span class="sxs-lookup"><span data-stu-id="790c8-118">Header</span></span></p></td><td><span data-ttu-id="790c8-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="790c8-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="790c8-120"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="790c8-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="790c8-121">**иоффлинеаналисискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="790c8-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
