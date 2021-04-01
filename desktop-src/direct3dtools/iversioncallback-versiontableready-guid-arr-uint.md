---
description: Функция обратного вызова, используемая для уведомления узла о том, какие интерфейсы поддерживаются.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иверсионкаллбакк:: Версионтаблереади'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140114"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="69781-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>Метод Иверсионкаллбакк:: Версионтаблереади</span><span class="sxs-lookup"><span data-stu-id="69781-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="69781-104">Функция обратного вызова, используемая для уведомления узла о том, какие интерфейсы поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="69781-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="69781-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69781-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="69781-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69781-106">Parameters</span></span>

<span data-ttu-id="69781-107">*count1 \_ интерфацеидс* </span><span class="sxs-lookup"><span data-stu-id="69781-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="69781-108">Массив, содержащий идентификаторы GUID поддерживаемых идентификаторов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="69781-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="69781-109">*расчета* </span><span class="sxs-lookup"><span data-stu-id="69781-109">*count* </span></span>  
<span data-ttu-id="69781-110">Число идентификаторов GUID, переданных в count1 \_ интерфацеидс.</span><span class="sxs-lookup"><span data-stu-id="69781-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="69781-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69781-111">Return value</span></span>

<span data-ttu-id="69781-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="69781-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69781-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69781-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69781-114">Требования</span><span class="sxs-lookup"><span data-stu-id="69781-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="69781-115">Header</span><span class="sxs-lookup"><span data-stu-id="69781-115">Header</span></span></p></td><td><span data-ttu-id="69781-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="69781-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="69781-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="69781-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="69781-118">**иверсионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="69781-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
