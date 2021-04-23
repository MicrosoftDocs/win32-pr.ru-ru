---
description: Обратный вызов, используемый для уведомления узла об обновлении объекта.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иупдатеобжекткаллбакк:: Упдатекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140115"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="9aa50-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Метод Иупдатеобжекткаллбакк:: Упдатекомплете</span><span class="sxs-lookup"><span data-stu-id="9aa50-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="9aa50-104">Обратный вызов, используемый для уведомления узла об обновлении объекта.</span><span class="sxs-lookup"><span data-stu-id="9aa50-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa50-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="9aa50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aa50-106">Parameters</span></span>

<span data-ttu-id="9aa50-107">*обжектаддресс* </span><span class="sxs-lookup"><span data-stu-id="9aa50-107">*objectAddress* </span></span>  
<span data-ttu-id="9aa50-108">Идентификатор объекта, который был обновлен.</span><span class="sxs-lookup"><span data-stu-id="9aa50-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="9aa50-109">*результат* </span><span class="sxs-lookup"><span data-stu-id="9aa50-109">*result* </span></span>  
<span data-ttu-id="9aa50-110">Указывает, было ли обновление удачным.</span><span class="sxs-lookup"><span data-stu-id="9aa50-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aa50-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aa50-111">Return value</span></span>

<span data-ttu-id="9aa50-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9aa50-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aa50-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9aa50-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa50-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9aa50-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9aa50-115">Header</span><span class="sxs-lookup"><span data-stu-id="9aa50-115">Header</span></span></p></td><td><span data-ttu-id="9aa50-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="9aa50-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9aa50-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="9aa50-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9aa50-118">**иупдатеобжекткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9aa50-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
