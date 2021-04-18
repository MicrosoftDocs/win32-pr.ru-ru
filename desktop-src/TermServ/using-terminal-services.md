---
title: Использование службы удаленных рабочих столов
description: Как программировать в среде службы удаленных рабочих столов и как расширять службы удаленных рабочих столов (ранее известные как службы терминалов) в Интернете с помощью веб-подключение к удаленному рабочему столу.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов службы удаленных рабочих столов с помощью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681458"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="ae46f-104">Использование службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="ae46f-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="ae46f-105">В следующих разделах описывается программирование в среде службы удаленных рабочих столов и расширение службы удаленных рабочих столов (ранее известной как службы терминалов) в Интернете с помощью веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="ae46f-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="ae46f-106">Если вы ищете сведения о пользователях удаленный рабочий стол, см. раздел [Подключение к другому компьютеру с помощью подключение к удаленному рабочему столу](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="ae46f-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="ae46f-107">Этот раздел предназначен для разработчиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ae46f-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="ae46f-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ae46f-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ae46f-109">Определение того, установлена ли роль службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="ae46f-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="ae46f-110">Пример кода C#, в котором показан метод, возвращающий **значение true** , если роль сервера службы удаленных рабочих столов установлена и запущена, или **значение false** в противном случае, начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ae46f-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-111">Расширение посредника сеансов служб терминалов</span><span class="sxs-lookup"><span data-stu-id="ae46f-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="ae46f-112">Посредник сеансов служб терминалов можно расширить с помощью COM-интерфейса [**ивтссбплугин**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="ae46f-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-113">Реализация пользовательского перечислителя конечной точки аудио</span><span class="sxs-lookup"><span data-stu-id="ae46f-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="ae46f-114">Начиная с Windows Server 2008 R2, можно реализовать настраиваемый перечислитель конечных точек удаленных аудио в составе поставщика удаленный рабочий стол протокола.</span><span class="sxs-lookup"><span data-stu-id="ae46f-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-115">Моникеры сеанса</span><span class="sxs-lookup"><span data-stu-id="ae46f-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="ae46f-116">Распределенная модель COM (DCOM) обеспечивает активацию объектов для каждого сеанса с помощью предоставленного системой моникера сеанса.</span><span class="sxs-lookup"><span data-stu-id="ae46f-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-117">Использование расширения ADSI для службы удаленных рабочих столов пользовательской конфигурации</span><span class="sxs-lookup"><span data-stu-id="ae46f-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="ae46f-118">Администрирование пользовательских свойств, связанных с службы удаленных рабочих столов, возможно с помощью методов, реализованных расширением интерфейсов служб Active Directory (ADSI), упакованных с помощью Tsuserex.dll библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="ae46f-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-119">Использование API службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="ae46f-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="ae46f-120">Описывает, как можно использовать API службы удаленных рабочих столов, чтобы позволить приложениям выполнять задачи в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ae46f-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-121">Использование API виртуализации удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="ae46f-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="ae46f-122">Разработчики могут использовать этот API для настройки логики, которую подключение к удаленному рабочему столу брокер (RDCB) для определения наилучшего назначения для входящего клиентского соединения.</span><span class="sxs-lookup"><span data-stu-id="ae46f-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ae46f-123">Интерфейс WSDL для пользовательских решений VDI</span><span class="sxs-lookup"><span data-stu-id="ae46f-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="ae46f-124">Разработчики могут создавать собственные веб-службы, которые управляют решениями инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="ae46f-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="ae46f-125">Дополнительные сведения см. в разделе [службы удаленных рабочих столов рекомендации по программированию](terminal-services-programming-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="ae46f-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae46f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ae46f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae46f-127">Службы терминалов теперь службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="ae46f-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="ae46f-128">Обнаружение среды службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="ae46f-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




