---
title: Отключение безопасности вызовов
description: Безопасность вызова определяет, имеет ли клиент разрешение на вызов методов сервера. Существует два способа отключения функции безопасности вызовов, который предполагает использование Dcomcnfg.exe для изменения реестра, а другой требует вызовов CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410723"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="bd7d9-104">Отключение безопасности вызовов</span><span class="sxs-lookup"><span data-stu-id="bd7d9-104">Turning Off Call Security</span></span>

<span data-ttu-id="bd7d9-105">Безопасность вызова определяет, имеет ли клиент разрешение на вызов методов сервера.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="bd7d9-106">Есть два способа отключить безопасность вызовов: одна из них включает использование Dcomcnfg.exe для изменения реестра, а другая требует вызовов [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="bd7d9-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="bd7d9-107">Отключение безопасности вызовов с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="bd7d9-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="bd7d9-108">Отключение безопасности вызова программным способом</span><span class="sxs-lookup"><span data-stu-id="bd7d9-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="bd7d9-109">См. также</span><span class="sxs-lookup"><span data-stu-id="bd7d9-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="bd7d9-110">Отключение безопасности вызовов с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="bd7d9-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="bd7d9-111">Безопасность вызова можно легко отключить с помощью Dcomcnfg.exe для изменения реестра.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="bd7d9-112">Однако использование Dcomcnfg.exe для отключения безопасности будет работать только в том случае, если клиент и сервер не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="bd7d9-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="bd7d9-113">Это связано с тем, что при вызове **COINITIALIZESECURITY** DCOM игнорирует параметры реестра и использует вместо них значения, указанные в **CoInitializeSecurity** .</span><span class="sxs-lookup"><span data-stu-id="bd7d9-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="bd7d9-114">Чтобы отключить безопасность с Dcomcnfg.exe, клиент и сервер должны установить уровень проверки подлинности None.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="bd7d9-115">Необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="bd7d9-116">Запустите файл Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="bd7d9-117">На странице **приложения** выберите приложение, представляющее сервер.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="bd7d9-118">Нажмите кнопку **Свойства** (или дважды щелкните выбранное приложение).</span><span class="sxs-lookup"><span data-stu-id="bd7d9-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="bd7d9-119">Перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="bd7d9-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="bd7d9-120">В списке **уровень проверки подлинности по умолчанию** выберите **(нет)**.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="bd7d9-121">Нажмите кнопку **Применить** , чтобы применить изменения. Однако изменения не применяются к работающим экземплярам приложения.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="bd7d9-122">Если клиент отображается в списке на странице *приложения* , повторите шаги с 2 по 5, выбрав клиент вместо сервера для шага 2.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="bd7d9-123">Затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-123">Then click the **OK** button.</span></span> <span data-ttu-id="bd7d9-124">Если клиент отсутствует в списке, можно выполнить одно из следующих трех действий.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="bd7d9-125">Для уровня проверки подлинности клиента можно установить значение "нет" на уровне компьютера с помощью Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="bd7d9-126">(См. предупреждение и процедуру ниже.)</span><span class="sxs-lookup"><span data-stu-id="bd7d9-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="bd7d9-127">Уровень проверки подлинности клиента можно задать равным Нет программными средствами.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="bd7d9-128">Можно создать ключ [AppID](appid-key.md) для клиента, чтобы указать уровень проверки подлинности None.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="bd7d9-129">(См. [раздел Настройка безопасности Process-Wide в реестре](setting-processwide-security-through-the-registry.md).)</span><span class="sxs-lookup"><span data-stu-id="bd7d9-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="bd7d9-130">Чтобы задать для уровня проверки подлинности значение "нет" на уровне компьютера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="bd7d9-131">Установка уровня проверки подлинности на уровне компьютера в значение «нет» чрезвычайно небезопасна.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="bd7d9-132">Запустите файл Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="bd7d9-133">Перейдите на вкладку **свойства по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="bd7d9-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="bd7d9-134">В списке **уровень проверки подлинности по умолчанию** выберите **(нет)**.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="bd7d9-135">Нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="bd7d9-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="bd7d9-136">Отключение безопасности вызова программным способом</span><span class="sxs-lookup"><span data-stu-id="bd7d9-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="bd7d9-137">Чтобы отключить безопасный вызов программным способом, клиент и сервер должны вызвать **CoInitializeSecurity**, установив уровень проверки подлинности в параметре *ДВАУСНЛЕВЕЛ* на \_ уровне RPC C \_ AUTHN \_ \_ None.</span><span class="sxs-lookup"><span data-stu-id="bd7d9-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd7d9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bd7d9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd7d9-139">Отключение безопасности активации</span><span class="sxs-lookup"><span data-stu-id="bd7d9-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




