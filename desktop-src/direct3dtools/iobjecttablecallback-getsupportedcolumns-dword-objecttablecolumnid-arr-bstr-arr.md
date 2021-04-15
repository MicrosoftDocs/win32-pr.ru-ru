---
description: Возвращает сведения о том, какие столбцы (типы данных объектов) поддерживаются таблицей объектов.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблекаллбакк:: Жетсуппортедколумнс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494709"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span data-ttu-id="e8e99-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Метод Иобжекттаблекаллбакк:: Жетсуппортедколумнс</span><span class="sxs-lookup"><span data-stu-id="e8e99-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns method</span></span>

<span data-ttu-id="e8e99-104">Возвращает сведения о том, какие столбцы (типы данных объектов) поддерживаются таблицей объектов.</span><span class="sxs-lookup"><span data-stu-id="e8e99-104">Gets information about which columns (types of object data) are supported by the object table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8e99-105">Syntax</span></span>


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="e8e99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8e99-106">Parameters</span></span>

<span data-ttu-id="e8e99-107">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="e8e99-107">*numColumns* </span></span>  
<span data-ttu-id="e8e99-108">Число столбцов, поддерживаемое таблицей объектов.</span><span class="sxs-lookup"><span data-stu-id="e8e99-108">The number of columns supported by the object table.</span></span>

<span data-ttu-id="e8e99-109">*count0_pIDs* </span><span class="sxs-lookup"><span data-stu-id="e8e99-109">*count0_pIDs* </span></span>  
<span data-ttu-id="e8e99-110">Идентификаторы каждого столбца, поддерживаемого таблицей объектов.</span><span class="sxs-lookup"><span data-stu-id="e8e99-110">The IDs of each column supported by the object table.</span></span>

<span data-ttu-id="e8e99-111">*count0_pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="e8e99-111">*count0_pBstrNames* </span></span>  
<span data-ttu-id="e8e99-112">Имена каждого столбца в виде строки COM, поддерживаемой таблицей объектов.</span><span class="sxs-lookup"><span data-stu-id="e8e99-112">The names of each column, as a COM string, supported by the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8e99-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8e99-113">Return value</span></span>

<span data-ttu-id="e8e99-114">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e8e99-114">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e8e99-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8e99-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e99-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e8e99-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e8e99-117">Header</span><span class="sxs-lookup"><span data-stu-id="e8e99-117">Header</span></span></p></td><td><span data-ttu-id="e8e99-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="e8e99-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e8e99-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="e8e99-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e8e99-120">**иобжекттаблекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e8e99-120">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
