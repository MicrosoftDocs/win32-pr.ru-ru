---
description: Функция обратного вызова, используемая для уведомления узла о данных таблицы объектов.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблекаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806695"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="ac5a4-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Метод Иобжекттаблекаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="ac5a4-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="ac5a4-104">Функция обратного вызова, используемая для уведомления узла о данных таблицы объектов.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac5a4-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="ac5a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac5a4-106">Parameters</span></span>

<span data-ttu-id="ac5a4-107">*нумелементс* </span><span class="sxs-lookup"><span data-stu-id="ac5a4-107">*numElements* </span></span>  
<span data-ttu-id="ac5a4-108">Общее число полей во всех столбцах всех объектов.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="ac5a4-109">*нумровс* </span><span class="sxs-lookup"><span data-stu-id="ac5a4-109">*numRows* </span></span>  
<span data-ttu-id="ac5a4-110">Число передаваемых объектов.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-110">The number of objects being transferred.</span></span>

<span data-ttu-id="ac5a4-111">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="ac5a4-111">*numColumns* </span></span>  
<span data-ttu-id="ac5a4-112">Количество столбцов (полей) данных, передаваемых для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="ac5a4-113">*count0 \_ провдата* </span><span class="sxs-lookup"><span data-stu-id="ac5a4-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="ac5a4-114">Сведения об объектах; по одному элементу для каждого поля каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac5a4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac5a4-115">Return value</span></span>

<span data-ttu-id="ac5a4-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ac5a4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac5a4-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac5a4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5a4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ac5a4-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ac5a4-119">Header</span><span class="sxs-lookup"><span data-stu-id="ac5a4-119">Header</span></span></p></td><td><span data-ttu-id="ac5a4-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="ac5a4-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ac5a4-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="ac5a4-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ac5a4-122">**иобжекттаблекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="ac5a4-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
