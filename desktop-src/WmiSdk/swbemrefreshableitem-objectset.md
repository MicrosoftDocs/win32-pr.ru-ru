---
description: Свойство Свбемрефрешаблеитем. Objecting представляет набор объектов для обновления.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: Свойство Свбемрефрешаблеитем. Objecting (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351385"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="83e89-103">Свбемрефрешаблеитем. Objecting, свойство</span><span class="sxs-lookup"><span data-stu-id="83e89-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="83e89-104">Свойство **свбемрефрешаблеитем. objecting** представляет набор объектов для обновления.</span><span class="sxs-lookup"><span data-stu-id="83e89-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="83e89-105">Свойство "набор **объектов** " является либо перечислителем, либо элементом сбора, содержащимся в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="83e89-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="83e89-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="83e89-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="83e89-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="83e89-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83e89-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="83e89-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="83e89-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="83e89-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83e89-110">Remarks</span></span>

<span data-ttu-id="83e89-111">Это свойство имеет **значение NULL** , если только [**свбемрефрешаблеитем. Иссет**](swbemrefreshableitem-isset.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="83e89-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e89-112">Требования</span><span class="sxs-lookup"><span data-stu-id="83e89-112">Requirements</span></span>



| <span data-ttu-id="83e89-113">Требование</span><span class="sxs-lookup"><span data-stu-id="83e89-113">Requirement</span></span> | <span data-ttu-id="83e89-114">Значение</span><span class="sxs-lookup"><span data-stu-id="83e89-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83e89-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83e89-115">Minimum supported client</span></span><br/> | <span data-ttu-id="83e89-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83e89-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83e89-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83e89-117">Minimum supported server</span></span><br/> | <span data-ttu-id="83e89-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83e89-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83e89-119">Header</span><span class="sxs-lookup"><span data-stu-id="83e89-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e89-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e89-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="83e89-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="83e89-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="83e89-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83e89-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83e89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="83e89-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e89-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83e89-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="83e89-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="83e89-125">CLSID</span></span><br/>                    | <span data-ttu-id="83e89-126">\_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID</span><span class="sxs-lookup"><span data-stu-id="83e89-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="83e89-127">IID</span><span class="sxs-lookup"><span data-stu-id="83e89-127">IID</span></span><br/>                      | <span data-ttu-id="83e89-128">IID \_ исвбемрефрешаблеитем</span><span class="sxs-lookup"><span data-stu-id="83e89-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="83e89-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83e89-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e89-130">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="83e89-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="83e89-131">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="83e89-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




