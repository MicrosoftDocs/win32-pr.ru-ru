---
description: Свойство Свбемрефрешаблеитем. Иссет является логическим значением, указывающим, представляет ли объект Свбемрефрешаблеитем один объект или набор объектов. Объект Свбемрефрешаблеитем представляет отдельный объект или набор объектов.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Свойство Свбемрефрешаблеитем. Иссет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693833"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="c7c3f-103">Свбемрефрешаблеитем. Иссет, свойство</span><span class="sxs-lookup"><span data-stu-id="c7c3f-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="c7c3f-104">Свойство **свбемрефрешаблеитем. Иссет** является логическим значением, указывающим, представляет ли объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) один объект или набор объектов.</span><span class="sxs-lookup"><span data-stu-id="c7c3f-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="c7c3f-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c7c3f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c7c3f-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c7c3f-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c3f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7c3f-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c7c3f-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c7c3f-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c3f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7c3f-109">Remarks</span></span>

<span data-ttu-id="c7c3f-110">Если **свбемрефрешаблеитем. Иссет** имеет **значение true**, то элемент представляет объект [**SWbemObjectSet**](swbemobjectset.md) , а свойство [**объекта**](swbemrefreshableitem-object.md) будет иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7c3f-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="c7c3f-111">Если **значение равно false**, элемент представляет объект [**SWbemObject**](swbemobject.md) , а свойство **объекта** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7c3f-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c3f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c7c3f-112">Requirements</span></span>



| <span data-ttu-id="c7c3f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c7c3f-113">Requirement</span></span> | <span data-ttu-id="c7c3f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c7c3f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c3f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7c3f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c3f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7c3f-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7c3f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7c3f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c3f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7c3f-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7c3f-119">Header</span><span class="sxs-lookup"><span data-stu-id="c7c3f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c3f-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c3f-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7c3f-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c7c3f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7c3f-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7c3f-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7c3f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c3f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c3f-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c3f-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7c3f-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="c7c3f-125">CLSID</span></span><br/>                    | <span data-ttu-id="c7c3f-126">\_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID</span><span class="sxs-lookup"><span data-stu-id="c7c3f-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="c7c3f-127">IID</span><span class="sxs-lookup"><span data-stu-id="c7c3f-127">IID</span></span><br/>                      | <span data-ttu-id="c7c3f-128">IID \_ исвбемрефрешаблеитем</span><span class="sxs-lookup"><span data-stu-id="c7c3f-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="c7c3f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7c3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c3f-130">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="c7c3f-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="c7c3f-131">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="c7c3f-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




