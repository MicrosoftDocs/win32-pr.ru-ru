---
description: Метод Свбемрефрешер. Item возвращает указанный Свбемрефрешаблеитем из коллекции. Свбемрефрешаблеитем из коллекции.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273254"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="11802-103">Свбемрефрешер. Item, метод</span><span class="sxs-lookup"><span data-stu-id="11802-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="11802-104">Метод **свбемрефрешер. Item** Возвращает указанный [**свбемрефрешаблеитем**](swbemrefreshableitem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="11802-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="11802-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="11802-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11802-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11802-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="11802-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="11802-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11802-108">*линдекс*</span><span class="sxs-lookup"><span data-stu-id="11802-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="11802-109">Значение индекса элемента в коллекции.</span><span class="sxs-lookup"><span data-stu-id="11802-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11802-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11802-110">Return value</span></span>

<span data-ttu-id="11802-111">Если вызов выполнен успешно, возвращается указанный объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="11802-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11802-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="11802-112">Error codes</span></span>

<span data-ttu-id="11802-113">Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.</span><span class="sxs-lookup"><span data-stu-id="11802-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="11802-114">Требования</span><span class="sxs-lookup"><span data-stu-id="11802-114">Requirements</span></span>



| <span data-ttu-id="11802-115">Требование</span><span class="sxs-lookup"><span data-stu-id="11802-115">Requirement</span></span> | <span data-ttu-id="11802-116">Значение</span><span class="sxs-lookup"><span data-stu-id="11802-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11802-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11802-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11802-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11802-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11802-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11802-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11802-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11802-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11802-121">Header</span><span class="sxs-lookup"><span data-stu-id="11802-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11802-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11802-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="11802-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="11802-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="11802-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11802-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11802-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11802-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11802-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11802-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="11802-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="11802-127">CLSID</span></span><br/>                    | <span data-ttu-id="11802-128">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="11802-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="11802-129">IID</span><span class="sxs-lookup"><span data-stu-id="11802-129">IID</span></span><br/>                      | <span data-ttu-id="11802-130">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="11802-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="11802-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11802-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11802-132">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="11802-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




