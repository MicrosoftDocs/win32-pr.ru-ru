---
description: Свойство манифеста используется для задания или получения активного контекста активации.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Акткткс. manifest, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991036"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="2eeb7-103">Акткткс. manifest, свойство</span><span class="sxs-lookup"><span data-stu-id="2eeb7-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="2eeb7-104">Свойство **манифеста** используется для задания или получения активного контекста активации.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="2eeb7-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eeb7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eeb7-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="2eeb7-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2eeb7-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2eeb7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2eeb7-108">Remarks</span></span>

<span data-ttu-id="2eeb7-109">Если контекст активации может быть создан с помощью предоставленного файла манифеста, то следующий скрипт задает свойство MANIFEST и активирует константу активации, указанную в манифесте.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="2eeb7-110">Если контекст активации не может быть создан из манифеста, контекст активации остается установленным в текущем активном контексте активации.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="2eeb7-111">Актктксобж. manifest = "<*имя файла манифеста*>";</span><span class="sxs-lookup"><span data-stu-id="2eeb7-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="2eeb7-112">Если контекст активации был ранее создан или активирован, то следующий скрипт задает свойство **manifest** для текущего контекста активации.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="2eeb7-113">Если контекст активации ранее не был создан или активирован, для свойства **манифеста** задается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="2eeb7-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="2eeb7-114">"BSTR Бстрманифест = Актктксобж. manifest"</span><span class="sxs-lookup"><span data-stu-id="2eeb7-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="2eeb7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2eeb7-115">Requirements</span></span>



| <span data-ttu-id="2eeb7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2eeb7-116">Requirement</span></span> | <span data-ttu-id="2eeb7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2eeb7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2eeb7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2eeb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eeb7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2eeb7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2eeb7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2eeb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eeb7-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2eeb7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2eeb7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2eeb7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eeb7-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eeb7-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="2eeb7-124">IID</span><span class="sxs-lookup"><span data-stu-id="2eeb7-124">IID</span></span><br/>                      | <span data-ttu-id="2eeb7-125">IID \_ иакткткс определен как 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="2eeb7-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




