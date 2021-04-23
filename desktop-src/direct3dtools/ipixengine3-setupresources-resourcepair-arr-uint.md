---
description: Передает ресурсы в подсистему, например строки для сообщений об ошибках.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine3:: Сетупресаурцес'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140138"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span data-ttu-id="6f951-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>Метод IPixEngine3:: Сетупресаурцес</span><span class="sxs-lookup"><span data-stu-id="6f951-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources method</span></span>

<span data-ttu-id="6f951-104">Передает ресурсы в подсистему, например строки для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6f951-104">Passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f951-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f951-105">Syntax</span></span>


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a><span data-ttu-id="6f951-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f951-106">Parameters</span></span>

<span data-ttu-id="6f951-107">*\_ресурсы count1* </span><span class="sxs-lookup"><span data-stu-id="6f951-107">*count1\_resources* </span></span>  
<span data-ttu-id="6f951-108">Переданные ресурсы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f951-108">The resources resources passed.</span></span>

<span data-ttu-id="6f951-109">*расчета* </span><span class="sxs-lookup"><span data-stu-id="6f951-109">*count* </span></span>  
<span data-ttu-id="6f951-110">Число переданных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f951-110">The number of resources passed.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f951-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f951-111">Return value</span></span>

<span data-ttu-id="6f951-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6f951-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f951-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f951-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f951-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6f951-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6f951-115">Header</span><span class="sxs-lookup"><span data-stu-id="6f951-115">Header</span></span></p></td><td><span data-ttu-id="6f951-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="6f951-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6f951-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="6f951-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6f951-118">**IPixEngine3**</span><span class="sxs-lookup"><span data-stu-id="6f951-118">**IPixEngine3**</span></span>](/windows/desktop/direct3dtools/ipixengine3)

 

 
