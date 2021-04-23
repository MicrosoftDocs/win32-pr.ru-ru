---
title: лаунчпермиссион
description: Описание списка управления доступом (ACL) участников, которые могут запускать новые серверы для этого класса. Это значение можно добавить в любой ключ AppID, чтобы ограничить активацию удаленными клиентами конкретных классов.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- COM-значение реестра Лаунчпермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068625"
---
# <a name="launchpermission"></a><span data-ttu-id="348d7-105">лаунчпермиссион</span><span class="sxs-lookup"><span data-stu-id="348d7-105">LaunchPermission</span></span>

<span data-ttu-id="348d7-106">Описание списка управления доступом (ACL) участников, которые могут запускать новые серверы для этого класса.</span><span class="sxs-lookup"><span data-stu-id="348d7-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="348d7-107">Это значение можно добавить в любой ключ [**AppID**](appid-key.md) , чтобы ограничить активацию удаленными клиентами конкретных классов.</span><span class="sxs-lookup"><span data-stu-id="348d7-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="348d7-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="348d7-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="348d7-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="348d7-109">Remarks</span></span>

<span data-ttu-id="348d7-110">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="348d7-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="348d7-111">После получения локального или удаленного запроса на запуск сервера этого класса список ACL, описываемый этим значением, проверяется при олицетворении клиента, и его успешное выполнение либо разрешает, либо запрещает запуск сервера.</span><span class="sxs-lookup"><span data-stu-id="348d7-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="348d7-112">Если это значение не существует, значение [**дефаултлаунчпермиссион**](defaultlaunchpermission.md) проверяется таким же образом, чтобы определить, можно ли запустить код класса.</span><span class="sxs-lookup"><span data-stu-id="348d7-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="348d7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="348d7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="348d7-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="348d7-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="348d7-115">**дефаултлаунчпермиссион**</span><span class="sxs-lookup"><span data-stu-id="348d7-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="348d7-116">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="348d7-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




