---
description: Свойство безопасности \_ объекта SWbemObjectSet используется для получения или задания параметров безопасности для объекта SWbemObjectSet. Это свойство является объектом Свбемсекурити.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Свойство SWbemObjectSet.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701945"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="0882b-104">SWbemObjectSet. Security, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="0882b-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="0882b-105">Свойство **безопасности \_** объекта [**SWbemObjectSet**](swbemobjectset.md) используется для получения или задания параметров безопасности для объекта **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="0882b-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="0882b-106">Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="0882b-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="0882b-107">Установка свойства [**безопасности \_**](swbemobject-security-.md) объекта [**SWbemObjectSet**](swbemobjectset.md) в **значение NULL** предоставляет всем пользователям неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="0882b-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="0882b-108">Дополнительные сведения о влиянии неограниченного доступа см. в разделе [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="0882b-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="0882b-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0882b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0882b-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0882b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0882b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0882b-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="0882b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0882b-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="0882b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0882b-113">Requirements</span></span>



| <span data-ttu-id="0882b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0882b-114">Requirement</span></span> | <span data-ttu-id="0882b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0882b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0882b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0882b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0882b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0882b-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0882b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0882b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0882b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0882b-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0882b-120">Header</span><span class="sxs-lookup"><span data-stu-id="0882b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0882b-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0882b-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0882b-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0882b-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0882b-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0882b-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0882b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0882b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0882b-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0882b-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0882b-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="0882b-126">CLSID</span></span><br/>                    | <span data-ttu-id="0882b-127">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="0882b-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="0882b-128">IID</span><span class="sxs-lookup"><span data-stu-id="0882b-128">IID</span></span><br/>                      | <span data-ttu-id="0882b-129">IID \_ исвбемобжектсет</span><span class="sxs-lookup"><span data-stu-id="0882b-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="0882b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0882b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0882b-131">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="0882b-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="0882b-132">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="0882b-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="0882b-133">Защита клиентов скриптов</span><span class="sxs-lookup"><span data-stu-id="0882b-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




