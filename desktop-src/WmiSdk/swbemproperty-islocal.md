---
description: Свойство Local объекта SWbemProperty является логическим значением, которое можно использовать, чтобы определить, является ли это свойство локальным. Значение FALSE указывает, что это свойство унаследовано от другого класса. Это свойство доступно только для чтения.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: Свойство SWbemProperty. local (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910275"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="72f3e-105">Свойство SWbemProperty. local</span><span class="sxs-lookup"><span data-stu-id="72f3e-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="72f3e-106">Свойство **Local** объекта [**SWbemProperty**](swbemproperty.md) является логическим значением, которое можно использовать, чтобы определить, является ли это свойство локальным.</span><span class="sxs-lookup"><span data-stu-id="72f3e-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="72f3e-107">Значение **false** указывает, что это свойство унаследовано от другого класса.</span><span class="sxs-lookup"><span data-stu-id="72f3e-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="72f3e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="72f3e-108">This property is read-only.</span></span>

<span data-ttu-id="72f3e-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="72f3e-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="72f3e-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="72f3e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f3e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72f3e-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="72f3e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="72f3e-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="72f3e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="72f3e-113">Requirements</span></span>



| <span data-ttu-id="72f3e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="72f3e-114">Requirement</span></span> | <span data-ttu-id="72f3e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="72f3e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72f3e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72f3e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="72f3e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72f3e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72f3e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72f3e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="72f3e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72f3e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72f3e-120">Header</span><span class="sxs-lookup"><span data-stu-id="72f3e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f3e-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f3e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f3e-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="72f3e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="72f3e-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72f3e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72f3e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="72f3e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f3e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f3e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72f3e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="72f3e-126">CLSID</span></span><br/>                    | <span data-ttu-id="72f3e-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="72f3e-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="72f3e-128">IID</span><span class="sxs-lookup"><span data-stu-id="72f3e-128">IID</span></span><br/>                      | <span data-ttu-id="72f3e-129">IID \_ исвбемпроперти</span><span class="sxs-lookup"><span data-stu-id="72f3e-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




