---
title: Имена субъектов-служб
description: Имя участника-службы (SPN) — это уникальный идентификатор экземпляра службы.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Имена субъектов-служб
- ИМЯ участника-службы см. в разделе имена участников-служб
- имя субъекта-службы AD
- имя субъекта-службы (AD), сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890371"
---
# <a name="service-principal-names"></a><span data-ttu-id="fffa9-107">Имена субъектов-служб</span><span class="sxs-lookup"><span data-stu-id="fffa9-107">Service Principal Names</span></span>

<span data-ttu-id="fffa9-108">Имя участника-службы (SPN) — это уникальный идентификатор экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="fffa9-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="fffa9-109">Имена участников-служб используются при [проверке подлинности Kerberos](mutual-authentication-using-kerberos.md) для связывания экземпляра службы с учетной записью входа службы.</span><span class="sxs-lookup"><span data-stu-id="fffa9-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="fffa9-110">Это позволяет клиентскому приложению запросить проверку подлинности учетной записи службы, даже если у клиента нет имени учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fffa9-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="fffa9-111">Если на компьютерах в лесу установлено несколько экземпляров службы, то каждый экземпляр должен иметь свое имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="fffa9-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="fffa9-112">Каждый экземпляр службы может иметь несколько имен участников-служб при наличии нескольких имен, которые могут использоваться клиентами для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fffa9-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="fffa9-113">Например, SPN всегда включает имя главного компьютера, на котором выполняется экземпляр службы, поэтому экземпляр службы может зарегистрировать имя участника-службы для каждого имени или псевдонима узла.</span><span class="sxs-lookup"><span data-stu-id="fffa9-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="fffa9-114">Дополнительные сведения о формате SPN и создании уникального имени субъекта-службы см. в разделе [форматы имен для уникальных имен участников-служб](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="fffa9-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="fffa9-115">Прежде чем служба проверки подлинности Kerberos сможет использовать имена участников-служб для проверки подлинности службы, имя участника-службы должно быть зарегистрировано в объекте учетной записи, используемом экземпляром службы для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="fffa9-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="fffa9-116">Данное имя субъекта-службы может быть зарегистрировано только в одной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fffa9-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="fffa9-117">Для служб Win32 установщик службы задает учетную запись входа при установке экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="fffa9-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="fffa9-118">Затем установщик формирует имена участников-служб и записывает их в качестве свойства объекта Account в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="fffa9-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="fffa9-119">При изменении учетной записи входа в экземпляр службы имена участников-служб должны быть повторно зарегистрированы в новой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fffa9-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="fffa9-120">Дополнительные сведения см. [в разделе как служба регистрирует свои имена участников-](how-a-service-registers-its-spns.md)служб.</span><span class="sxs-lookup"><span data-stu-id="fffa9-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="fffa9-121">Когда клиент хочет подключиться к службе, он определяет местонахождение экземпляра службы, составляет для него основное имя, подключается к службе и представляет ей это имя для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fffa9-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="fffa9-122">Дополнительные сведения см. [в разделе как клиенты составлять имена участников-служб Службы](how-clients-compose-a-serviceampaposs-spn.md).</span><span class="sxs-lookup"><span data-stu-id="fffa9-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fffa9-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="fffa9-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fffa9-124">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="fffa9-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fffa9-125">Форматы имен для уникальных имен участников-служб</span><span class="sxs-lookup"><span data-stu-id="fffa9-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="fffa9-126">Как служба формирует свои имена участников-служб</span><span class="sxs-lookup"><span data-stu-id="fffa9-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="fffa9-127">Как служба регистрирует свои имена участников-служб</span><span class="sxs-lookup"><span data-stu-id="fffa9-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="fffa9-128">Создание клиентами SPN службы</span><span class="sxs-lookup"><span data-stu-id="fffa9-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="fffa9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fffa9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fffa9-130">Что такое SPN и зачем вам нужно заниматься?</span><span class="sxs-lookup"><span data-stu-id="fffa9-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="fffa9-131">Взаимная проверка подлинности с помощью Kerberos</span><span class="sxs-lookup"><span data-stu-id="fffa9-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 