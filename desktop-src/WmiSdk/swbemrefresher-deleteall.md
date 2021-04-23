---
description: Метод Свбемрефрешер. DeleteAll удаляет все элементы из коллекции в объекте Свбемрефрешер. Объект Свбемрефрешер.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Свбемрефрешер. DeleteAll, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703461"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="9a47b-103">Свбемрефрешер. DeleteAll, метод</span><span class="sxs-lookup"><span data-stu-id="9a47b-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="9a47b-104">Метод **свбемрефрешер. DeleteAll** удаляет все элементы из коллекции в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="9a47b-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="9a47b-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9a47b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a47b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a47b-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="9a47b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a47b-107">Parameters</span></span>

<span data-ttu-id="9a47b-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9a47b-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a47b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a47b-109">Return value</span></span>

<span data-ttu-id="9a47b-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a47b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a47b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a47b-111">Remarks</span></span>

<span data-ttu-id="9a47b-112">В соответствующем [**свбемрефрешаблеитем**](swbemrefreshableitem.md) для каждого удаленного элемента свойство [**Обновитель**](swbemrefreshableitem-refresher.md) имеет значение **null**, которое указывает, что у него больше нет родительского обновления.</span><span class="sxs-lookup"><span data-stu-id="9a47b-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a47b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9a47b-113">Requirements</span></span>



| <span data-ttu-id="9a47b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9a47b-114">Requirement</span></span> | <span data-ttu-id="9a47b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9a47b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a47b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a47b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a47b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a47b-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a47b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a47b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a47b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a47b-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a47b-120">Header</span><span class="sxs-lookup"><span data-stu-id="9a47b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a47b-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a47b-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a47b-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9a47b-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a47b-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a47b-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a47b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9a47b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a47b-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a47b-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a47b-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="9a47b-126">CLSID</span></span><br/>                    | <span data-ttu-id="9a47b-127">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9a47b-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="9a47b-128">IID</span><span class="sxs-lookup"><span data-stu-id="9a47b-128">IID</span></span><br/>                      | <span data-ttu-id="9a47b-129">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="9a47b-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="9a47b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a47b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a47b-131">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="9a47b-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




