---
description: Свойство безопасности объекта Свбемобжектпас используется для получения или задания компонентов безопасности пути к объекту.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Свойство SWbemObjectPath.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263796"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="ae880-103">Свбемобжектпас. Security, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="ae880-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="ae880-104">Свойство **безопасности** объекта [**свбемобжектпас**](swbemobjectpath.md) используется для получения или задания компонентов безопасности пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="ae880-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="ae880-105">Обратите внимание, что он не используется для установки атрибутов безопасности самого объекта **свбемобжектпас** .</span><span class="sxs-lookup"><span data-stu-id="ae880-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="ae880-106">Он используется только для представления компонентов безопасности пути к объекту [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="ae880-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="ae880-107">Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="ae880-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="ae880-108">Установка свойства [**безопасности \_**](swbemobject-security-.md) объекта [**свбемобжектпас**](swbemobjectset.md) в **значение NULL** предоставляет всем пользователям неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="ae880-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="ae880-109">Дополнительные сведения см. в разделе [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ae880-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="ae880-110">Дополнительные сведения см. [в разделе соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ae880-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ae880-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ae880-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae880-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae880-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="ae880-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ae880-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ae880-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ae880-114">Requirements</span></span>



| <span data-ttu-id="ae880-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ae880-115">Requirement</span></span> | <span data-ttu-id="ae880-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ae880-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae880-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae880-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae880-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae880-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae880-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae880-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae880-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae880-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae880-121">Header</span><span class="sxs-lookup"><span data-stu-id="ae880-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae880-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae880-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae880-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ae880-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae880-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae880-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae880-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ae880-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae880-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae880-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae880-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae880-127">CLSID</span></span><br/>                    | <span data-ttu-id="ae880-128">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="ae880-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="ae880-129">IID</span><span class="sxs-lookup"><span data-stu-id="ae880-129">IID</span></span><br/>                      | <span data-ttu-id="ae880-130">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="ae880-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="ae880-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae880-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae880-132">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="ae880-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="ae880-133">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="ae880-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="ae880-134">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="ae880-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




