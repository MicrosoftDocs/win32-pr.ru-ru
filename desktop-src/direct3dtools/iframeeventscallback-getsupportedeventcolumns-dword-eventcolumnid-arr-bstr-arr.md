---
description: Возвращает сведения о том, какие столбцы (типы данных событий) поддерживаются списком событий.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентскаллбакк:: Жетсуппортедевентколумнс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495210"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="f2124-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>Метод Ифрамивентскаллбакк:: Жетсуппортедевентколумнс</span><span class="sxs-lookup"><span data-stu-id="f2124-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="f2124-104">Возвращает сведения о том, какие столбцы (типы данных событий) поддерживаются списком событий.</span><span class="sxs-lookup"><span data-stu-id="f2124-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2124-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2124-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="f2124-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2124-106">Parameters</span></span>

<span data-ttu-id="f2124-107">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="f2124-107">*numColumns* </span></span>  
<span data-ttu-id="f2124-108">Число столбцов, поддерживаемое</span><span class="sxs-lookup"><span data-stu-id="f2124-108">The number of columns supported by</span></span>

<span data-ttu-id="f2124-109">*count0 \_ PID* </span><span class="sxs-lookup"><span data-stu-id="f2124-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="f2124-110">Идентификаторы каждого столбца, поддерживаемого списком событий.</span><span class="sxs-lookup"><span data-stu-id="f2124-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="f2124-111">*count0 \_ пбстрнамес* </span><span class="sxs-lookup"><span data-stu-id="f2124-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="f2124-112">Имена каждого столбца в виде строки COM, поддерживаемой списком событий.</span><span class="sxs-lookup"><span data-stu-id="f2124-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2124-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2124-113">Return value</span></span>

<span data-ttu-id="f2124-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2124-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2124-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2124-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2124-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f2124-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f2124-117">Header</span><span class="sxs-lookup"><span data-stu-id="f2124-117">Header</span></span></p></td><td><span data-ttu-id="f2124-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f2124-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f2124-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="f2124-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f2124-120">**ифрамивентскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f2124-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
