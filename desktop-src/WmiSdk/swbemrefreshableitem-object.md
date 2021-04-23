---
description: Свойство Свбемрефрешаблеитем. Object представляет один экземпляр SWbemObject, который обновляется. Элемент содержится в объекте Свбемрефрешер. Обновляемый экземпляр SWbemObject. Элемент содержится в объекте Свбемрефрешер.
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: Свойство Свбемрефрешаблеитем. Object (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999904"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="ac829-105">Свбемрефрешаблеитем. Object, свойство</span><span class="sxs-lookup"><span data-stu-id="ac829-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="ac829-106">Свойство **свбемрефрешаблеитем. Object** представляет один экземпляр [**SWbemObject**](swbemobject.md) , который обновляется.</span><span class="sxs-lookup"><span data-stu-id="ac829-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="ac829-107">Элемент содержится в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="ac829-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="ac829-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ac829-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ac829-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ac829-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac829-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac829-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="ac829-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac829-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ac829-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac829-112">Remarks</span></span>

<span data-ttu-id="ac829-113">Это свойство имеет **значение NULL** , если только [**свбемрефрешаблеитем. Иссет**](swbemrefreshableitem-isset.md) имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ac829-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac829-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ac829-114">Requirements</span></span>



| <span data-ttu-id="ac829-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ac829-115">Requirement</span></span> | <span data-ttu-id="ac829-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ac829-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac829-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac829-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ac829-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac829-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac829-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac829-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ac829-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac829-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac829-121">Header</span><span class="sxs-lookup"><span data-stu-id="ac829-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac829-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac829-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac829-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ac829-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac829-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ac829-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ac829-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac829-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac829-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac829-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ac829-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="ac829-127">CLSID</span></span><br/>                    | <span data-ttu-id="ac829-128">\_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID</span><span class="sxs-lookup"><span data-stu-id="ac829-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="ac829-129">IID</span><span class="sxs-lookup"><span data-stu-id="ac829-129">IID</span></span><br/>                      | <span data-ttu-id="ac829-130">IID \_ исвбемрефрешаблеитем</span><span class="sxs-lookup"><span data-stu-id="ac829-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="ac829-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac829-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac829-132">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="ac829-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="ac829-133">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="ac829-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




