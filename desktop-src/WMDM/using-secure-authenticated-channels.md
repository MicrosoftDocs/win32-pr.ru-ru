---
title: Использование защищенных каналов с проверкой подлинности
description: Использование защищенных каналов с проверкой подлинности
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Диспетчер устройств Windows Media, проверка подлинности
- Диспетчер устройств, проверка подлинности
- Классические приложения, проверка подлинности
- поставщики услуг, проверка подлинности
- инструкции по программированию, проверка подлинности
- проверка подлинности
- Windows Media диспетчер устройств, безопасное подключение
- Диспетчер устройств, безопасное взаимодействие
- Классические приложения, безопасное взаимодействие
- поставщики услуг, безопасное взаимодействие
- программное обеспечение, безопасное взаимодействие
- Безопасная связь
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067603"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="e20cf-115">Использование защищенных каналов с проверкой подлинности</span><span class="sxs-lookup"><span data-stu-id="e20cf-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="e20cf-116">Windows Media диспетчер устройств обеспечивает проверку подлинности и безопасный обмен данными между компонентами, предоставляя два вспомогательных класса: [ксекуречаннелклиент](csecurechannelclient-class.md) (для приложений) и [ксекуречаннелсервер](csecurechannelserver-class.md) (для поставщиков услуг) и один интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (для обоих).</span><span class="sxs-lookup"><span data-stu-id="e20cf-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="e20cf-117">Вместе они составляют API для использования защищенных каналов с проверкой подлинности (SAC).</span><span class="sxs-lookup"><span data-stu-id="e20cf-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="e20cf-118">Специальная консоль администрирования (SAC) обрабатывает следующие три задачи для поставщиков услуг или приложений, использующих Windows Media диспетчер устройств:</span><span class="sxs-lookup"><span data-stu-id="e20cf-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="e20cf-119">Проверка подлинности компонента</span><span class="sxs-lookup"><span data-stu-id="e20cf-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="e20cf-120">Шифрование и расшифровка</span><span class="sxs-lookup"><span data-stu-id="e20cf-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="e20cf-121">Проверка подлинности сообщений</span><span class="sxs-lookup"><span data-stu-id="e20cf-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="e20cf-122">Поставщик приложения или службы должен поддерживать проверку подлинности, шифрование и расшифровку компонента. Проверка подлинности сообщений является необязательной.</span><span class="sxs-lookup"><span data-stu-id="e20cf-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e20cf-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e20cf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e20cf-124">**Задачи, общие для приложений и поставщиков служб**</span><span class="sxs-lookup"><span data-stu-id="e20cf-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




