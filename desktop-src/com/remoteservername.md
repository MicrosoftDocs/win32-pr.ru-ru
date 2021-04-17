---
title: ремотесервернаме
description: Настраивает Клиент для запроса запуска объекта на определенном компьютере при вызове функции активации, для которой не указана структура КОСЕРВЕРИНФО.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- COM-значение реестра Ремотесервернаме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700953"
---
# <a name="remoteservername"></a><span data-ttu-id="ac48e-104">ремотесервернаме</span><span class="sxs-lookup"><span data-stu-id="ac48e-104">RemoteServerName</span></span>

<span data-ttu-id="ac48e-105">Настраивает Клиент для запроса запуска объекта на определенном компьютере при вызове функции активации, для которой не указана структура [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .</span><span class="sxs-lookup"><span data-stu-id="ac48e-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ac48e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="ac48e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="ac48e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac48e-107">Remarks</span></span>

<span data-ttu-id="ac48e-108">**Ремотесервернаме** обеспечивает простое управление конфигурацией клиентских приложений; они могут быть написаны без жестко заданных имен серверов и могут быть настроены путем изменения значений реестра **ремотесервернаме** классов объектов, которые они используют.</span><span class="sxs-lookup"><span data-stu-id="ac48e-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="ac48e-109">Как описано в документации по перечислению [**клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) и структуре [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , один из параметров распределенной активации com является указателем на структуру **косерверинфо** .</span><span class="sxs-lookup"><span data-stu-id="ac48e-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="ac48e-110">Если это значение не **равно NULL**, информация в структуре **косерверинфо** переопределяет значение ключа **ремотесервернаме** для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="ac48e-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac48e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="ac48e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac48e-112">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="ac48e-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 