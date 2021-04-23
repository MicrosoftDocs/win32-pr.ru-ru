---
description: Запросы на запуск эксперимента (записи) в указанном процессе.
MS-HAID: vspixengine.IRunExperimentCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ирунексперименткаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C00034DF-5F51-49A2-B49A-62F98EA48F46
api_name:
- IRunExperimentCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ac6838e7103970d588814bdc5a39e9e26fd4a33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710587"
---
# <a name="span-idvspixengineirunexperimentcallback_resultcallback_dwordspanirunexperimentcallbackresultcallback-method"></a><span data-ttu-id="3652b-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>Метод Ирунексперименткаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="3652b-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback::ResultCallback method</span></span>

<span data-ttu-id="3652b-104">Запросы на запуск эксперимента (записи) в указанном процессе.</span><span class="sxs-lookup"><span data-stu-id="3652b-104">Requests to run an experiment (capture) on the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="3652b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3652b-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD processId
);
```

## <a name="parameters"></a><span data-ttu-id="3652b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3652b-106">Parameters</span></span>

<span data-ttu-id="3652b-107">*processId* </span><span class="sxs-lookup"><span data-stu-id="3652b-107">*processId* </span></span>  
<span data-ttu-id="3652b-108">Указанный процесс.</span><span class="sxs-lookup"><span data-stu-id="3652b-108">The specified process.</span></span>

## <a name="return-value"></a><span data-ttu-id="3652b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3652b-109">Return value</span></span>

<span data-ttu-id="3652b-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3652b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3652b-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3652b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3652b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3652b-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3652b-113">Header</span><span class="sxs-lookup"><span data-stu-id="3652b-113">Header</span></span></p></td><td><span data-ttu-id="3652b-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="3652b-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3652b-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="3652b-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3652b-116">**ирунексперименткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3652b-116">**IRunExperimentCallback**</span></span>](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
