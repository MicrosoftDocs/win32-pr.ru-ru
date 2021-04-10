---
title: аусентикатионлевел
description: Задает уровень проверки подлинности для приложений, которые не вызывают CoInitializeSecurity, или для приложений, которые вызывают CoInitializeSecurity, и укажите AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- COM-значение реестра Аусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332635"
---
# <a name="authenticationlevel"></a><span data-ttu-id="1c49b-104">аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="1c49b-104">AuthenticationLevel</span></span>

<span data-ttu-id="1c49b-105">Задает уровень проверки подлинности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , или для приложений, которые вызывают **CoInitializeSecurity** , и укажите AppID.</span><span class="sxs-lookup"><span data-stu-id="1c49b-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1c49b-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="1c49b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="1c49b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c49b-107">Remarks</span></span>

<span data-ttu-id="1c49b-108">Это значение **reg \_ DWORD** , эквивалентное \_ \_ \_ константам уровня RPC C AUTHN.</span><span class="sxs-lookup"><span data-stu-id="1c49b-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="1c49b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1c49b-109">Value</span></span> | <span data-ttu-id="1c49b-110">Константа</span><span class="sxs-lookup"><span data-stu-id="1c49b-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="1c49b-111">1</span><span class="sxs-lookup"><span data-stu-id="1c49b-111">1</span></span>     | <span data-ttu-id="1c49b-112">\_уровень RPC \_ C \_ AUTHN \_ None</span><span class="sxs-lookup"><span data-stu-id="1c49b-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="1c49b-113">2</span><span class="sxs-lookup"><span data-stu-id="1c49b-113">2</span></span>     | <span data-ttu-id="1c49b-114">\_подключение на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="1c49b-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="1c49b-115">3</span><span class="sxs-lookup"><span data-stu-id="1c49b-115">3</span></span>     | <span data-ttu-id="1c49b-116">\_ \_ \_ вызов уровня RPC C \_ AUTHN</span><span class="sxs-lookup"><span data-stu-id="1c49b-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="1c49b-117">4</span><span class="sxs-lookup"><span data-stu-id="1c49b-117">4</span></span>     | <span data-ttu-id="1c49b-118">\_PKT на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="1c49b-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="1c49b-119">5</span><span class="sxs-lookup"><span data-stu-id="1c49b-119">5</span></span>     | <span data-ttu-id="1c49b-120">\_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_</span><span class="sxs-lookup"><span data-stu-id="1c49b-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="1c49b-121">6</span><span class="sxs-lookup"><span data-stu-id="1c49b-121">6</span></span>     | <span data-ttu-id="1c49b-122">\_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_</span><span class="sxs-lookup"><span data-stu-id="1c49b-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="1c49b-123">Значение **аусентикатионлевел** аналогично значению [**легациаусентикатионлевел**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="1c49b-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="1c49b-124">Если указано значение **аусентикатионлевел** , оно используется вместо значения **Легациаусентикатионлевел** для этого AppID.</span><span class="sxs-lookup"><span data-stu-id="1c49b-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="1c49b-125">Если значение **аусентикатионлевел** имеет неправильный тип или выходит за пределы допустимого диапазона, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) завершается ошибкой, что приводит к сбою упаковки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1c49b-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="1c49b-126">Это не позволяет приложению выполнять любые вызовы (между апартаментами, перекрестными потоками, межпроцессными и перекрестными компьютерами).</span><span class="sxs-lookup"><span data-stu-id="1c49b-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="1c49b-127">Значения **аусентикатионлевел** и [**акцесспермиссион**](accesspermission.md) независимы.</span><span class="sxs-lookup"><span data-stu-id="1c49b-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="1c49b-128">Если такой объект отсутствует, используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c49b-128">If one is not present, the default is used.</span></span> <span data-ttu-id="1c49b-129">В следующих правилах перечисляются взаимодействия между значением **аусентикатионлевел** и значением **акцесспермиссион** :</span><span class="sxs-lookup"><span data-stu-id="1c49b-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="1c49b-130">Если **аусентикатионлевел** имеет значение None, значения [**акцесспермиссион**](accesspermission.md) и [**дефаултакцесспермиссион**](defaultaccesspermission.md) игнорируются (для этого приложения).</span><span class="sxs-lookup"><span data-stu-id="1c49b-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="1c49b-131">Если **аусентикатионлевел** отсутствует и [**ЛЕГАЦИАУСЕНТИКАТИОНЛЕВЕЛ**](legacyauthenticationlevel.md) имеет значение None, значения [**акцесспермиссион**](accesspermission.md) и [**дефаултакцесспермиссион**](defaultaccesspermission.md) игнорируются (для этого приложения).</span><span class="sxs-lookup"><span data-stu-id="1c49b-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c49b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1c49b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c49b-133">Константы уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="1c49b-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="1c49b-134">**легациаусентикатионлевел**</span><span class="sxs-lookup"><span data-stu-id="1c49b-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="1c49b-135">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="1c49b-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="1c49b-136">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="1c49b-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




