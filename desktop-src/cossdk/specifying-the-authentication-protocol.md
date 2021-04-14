---
description: Указание протокола проверки подлинности
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Указание протокола проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496320"
---
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="aa86e-103">Указание протокола проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="aa86e-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="aa86e-104">В зависимости от требований безопасности на сайте, служба очередей компонентов всегда может потребовать от службы "компоненты очереди" проверять удостоверение клиента, никогда не проверять удостоверение клиента или проверять удостоверение клиента только в том случае, если компонент настроен на требование проверки подлинности даже при отсутствии доступа к очереди.</span><span class="sxs-lookup"><span data-stu-id="aa86e-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="aa86e-105">Чтобы использовать компонент в очереди в режиме рабочей группы, необходимо установить уровень проверки подлинности None.</span><span class="sxs-lookup"><span data-stu-id="aa86e-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="aa86e-106">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="aa86e-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="aa86e-107">Чтобы указать протокол проверки подлинности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="aa86e-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="aa86e-108">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым вы хотите управлять.</span><span class="sxs-lookup"><span data-stu-id="aa86e-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="aa86e-109">Щелкните правой кнопкой мыши приложение в очереди, для которого необходимо указать протокол проверки подлинности, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="aa86e-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="aa86e-110">Выберите вкладку **очередь** в диалоговом окне Свойства.</span><span class="sxs-lookup"><span data-stu-id="aa86e-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="aa86e-111">В разделе **Проверка подлинности сообщений MSMQ** выберите переключатель, связанный с протоколом проверки подлинности, который требуется реализовать.</span><span class="sxs-lookup"><span data-stu-id="aa86e-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="aa86e-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa86e-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="aa86e-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aa86e-113">Visual Basic</span></span>

<span data-ttu-id="aa86e-114">Используйте параметр *AUTHLEVEL* при активации приложения в очереди, как описано в разделе [Использование моникера очереди](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="aa86e-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="aa86e-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="aa86e-115">C/C++</span></span>

<span data-ttu-id="aa86e-116">Используйте параметр *AUTHLEVEL* при активации приложения в очереди, как описано в разделе [Использование моникера очереди](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="aa86e-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa86e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="aa86e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa86e-118">Безопасность очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="aa86e-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="aa86e-119">Ограничения безопасности в режиме рабочей группы</span><span class="sxs-lookup"><span data-stu-id="aa86e-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



