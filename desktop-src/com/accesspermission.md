---
title: акцесспермиссион
description: Описывает список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса. Этот список ACL используется только приложениями, которые не вызывают CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- COM-значение реестра Акцесспермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488313"
---
# <a name="accesspermission"></a><span data-ttu-id="75c9f-105">акцесспермиссион</span><span class="sxs-lookup"><span data-stu-id="75c9f-105">AccessPermission</span></span>

<span data-ttu-id="75c9f-106">Описывает список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса.</span><span class="sxs-lookup"><span data-stu-id="75c9f-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="75c9f-107">Этот список ACL используется только приложениями, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="75c9f-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="75c9f-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="75c9f-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="75c9f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75c9f-109">Remarks</span></span>

<span data-ttu-id="75c9f-110">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="75c9f-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="75c9f-111">Он содержит данные, описывающие список управления доступом (ACL) участников, которые могут обращаться к экземплярам этого класса.</span><span class="sxs-lookup"><span data-stu-id="75c9f-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="75c9f-112">При получении запроса на подключение к существующему объекту этого класса ACL проверяется с помощью вызываемого приложения при олицетворении вызывающего.</span><span class="sxs-lookup"><span data-stu-id="75c9f-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="75c9f-113">Если проверка доступа завершается сбоем, подключение запрещено.</span><span class="sxs-lookup"><span data-stu-id="75c9f-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="75c9f-114">Если это именованное значение не существует, список ACL [**дефаултакцесспермиссион**](defaultaccesspermission.md) проверяется, чтобы определить, должно ли быть разрешено подключение.</span><span class="sxs-lookup"><span data-stu-id="75c9f-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="75c9f-115">Для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) или не используют интерфейс [**Иглобалоптионс**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) для указания AppID, исполняемый файл двоичного приложения должен быть сопоставлен с AppID приложения, как описано в [**AppID**](appid.md).</span><span class="sxs-lookup"><span data-stu-id="75c9f-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="75c9f-116">Это необходимо для того, чтобы COM мог нахождение идентификатора AppID приложения.</span><span class="sxs-lookup"><span data-stu-id="75c9f-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c9f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="75c9f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c9f-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="75c9f-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="75c9f-119">**дефаултакцесспермиссион**</span><span class="sxs-lookup"><span data-stu-id="75c9f-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="75c9f-120">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="75c9f-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 