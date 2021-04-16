---
description: Задиктовать центр пакетов приложений.
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: Константы SID контейнера приложений (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651012"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="4b63e-103">Константы SID контейнера приложений</span><span class="sxs-lookup"><span data-stu-id="4b63e-103">App Container SID Constants</span></span>

<span data-ttu-id="4b63e-104">Константы SID, относящиеся к контейнеру приложения, определяют центр пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="4b63e-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="4b63e-105">Хотя разработчик может использовать эти константы напрямую, большинство разработчиков не нуждаются в определении этих идентификаторов безопасности контейнеров приложений.</span><span class="sxs-lookup"><span data-stu-id="4b63e-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="4b63e-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**Безопасность \_ \_ \_ Центр** приложений безопасности {0,0,0,0,0,15} <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **\_ \_ \_ Base \_ RID** (0x00000002L) встроенного приложения безопасности Идентификатор RID для пакета приложения <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> безопасности (2L) номер **\_ \_ \_ \_ \_** <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **\_ \_ \_ RID \_** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **основы безопасности \_ \_ Базовый \_ RID** (0x00000003L) встроенная функция безопасности Идентификатор RID (2L) функция обеспечения безопасности (5L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **\_ \_ \_ \_** <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> **\_ \_ \_** <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **\_ встроенный \_ пакет \_ всех \_ пакетов** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4b63e-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="4b63e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="4b63e-107">Requirements</span></span>



| <span data-ttu-id="4b63e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="4b63e-108">Requirement</span></span> | <span data-ttu-id="4b63e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="4b63e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b63e-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b63e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4b63e-111">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4b63e-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b63e-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b63e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4b63e-113">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4b63e-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4b63e-114">Header</span><span class="sxs-lookup"><span data-stu-id="4b63e-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b63e-115"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b63e-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




