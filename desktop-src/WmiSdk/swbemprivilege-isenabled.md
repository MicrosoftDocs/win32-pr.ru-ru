---
description: Свойство включил объекта Свбемпривилеже — это логическое значение, которое используется для включения или отключения этой привилегии. Дополнительные сведения о последствиях включения определенных привилегий см. в разделе выполнение с особыми привилегиями.
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: Свойство Свбемпривилеже. Enable (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701944"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="dc44b-104">Свбемпривилеже. Enable, свойство</span><span class="sxs-lookup"><span data-stu-id="dc44b-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="dc44b-105">Свойство **включил** объекта [**Свбемпривилеже**](swbemprivilege.md) — это логическое значение, которое используется для включения или отключения этой привилегии.</span><span class="sxs-lookup"><span data-stu-id="dc44b-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="dc44b-106">Дополнительные сведения о последствиях включения определенных привилегий см. в разделе [**выполнение с особыми привилегиями**](swbemsecurity-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="dc44b-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="dc44b-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dc44b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="dc44b-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dc44b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc44b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc44b-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="dc44b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dc44b-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="dc44b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dc44b-111">Requirements</span></span>



| <span data-ttu-id="dc44b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dc44b-112">Requirement</span></span> | <span data-ttu-id="dc44b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dc44b-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc44b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc44b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dc44b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc44b-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc44b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc44b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dc44b-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc44b-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc44b-118">Header</span><span class="sxs-lookup"><span data-stu-id="dc44b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc44b-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc44b-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc44b-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dc44b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc44b-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc44b-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc44b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dc44b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc44b-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc44b-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc44b-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="dc44b-124">CLSID</span></span><br/>                    | <span data-ttu-id="dc44b-125">\_СВБЕМПРИВИЛЕЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="dc44b-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="dc44b-126">IID</span><span class="sxs-lookup"><span data-stu-id="dc44b-126">IID</span></span><br/>                      | <span data-ttu-id="dc44b-127">IID \_ исвбемпривилеже</span><span class="sxs-lookup"><span data-stu-id="dc44b-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




