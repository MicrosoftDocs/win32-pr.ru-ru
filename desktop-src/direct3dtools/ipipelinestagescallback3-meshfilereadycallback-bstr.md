---
description: Обратный вызов, уведомляющий узел о размещении сведений о сетке, записанных связанным запросом.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback3:: Мешфилереадикаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673007"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="8ace1-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>Метод IPipeLineStagesCallback3:: Мешфилереадикаллбакк</span><span class="sxs-lookup"><span data-stu-id="8ace1-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="8ace1-104">Обратный вызов, уведомляющий узел о размещении сведений о сетке, записанных связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="8ace1-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ace1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ace1-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="8ace1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ace1-106">Parameters</span></span>

<span data-ttu-id="8ace1-107">*мешфиленаме* </span><span class="sxs-lookup"><span data-stu-id="8ace1-107">*meshFilename* </span></span>  
<span data-ttu-id="8ace1-108">Строка COM, содержащая путь к файлу, в который записываются данные сетки.</span><span class="sxs-lookup"><span data-stu-id="8ace1-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ace1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ace1-109">Return value</span></span>

<span data-ttu-id="8ace1-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ace1-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ace1-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ace1-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ace1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8ace1-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8ace1-113">Header</span><span class="sxs-lookup"><span data-stu-id="8ace1-113">Header</span></span></p></td><td><span data-ttu-id="8ace1-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8ace1-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8ace1-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="8ace1-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8ace1-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="8ace1-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
