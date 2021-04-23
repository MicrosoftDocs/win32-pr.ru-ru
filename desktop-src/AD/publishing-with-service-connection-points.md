---
title: Публикация с точками подключения службы
description: Схема Active Directory определяет класс объектов serviceConnectionPoint (SCP), чтобы служба может легко публиковать в каталоге данные, относящиеся к службе.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Публикация с помощью точек подключения службы AD
- точки подключения службы AD
- точки подключения службы AD, публикация с помощью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773112"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="5c7eb-106">Публикация с точками подключения службы</span><span class="sxs-lookup"><span data-stu-id="5c7eb-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="5c7eb-107">Схема Active Directory определяет класс объектов **serviceConnectionPoint** (SCP), чтобы служба может легко публиковать в каталоге данные, относящиеся к службе.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="5c7eb-108">Клиенты службы используют данные в SCP для нахождения, подключения и проверки подлинности экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="5c7eb-109">В этом разделе приводятся общие сведения о точках подключения службы и примеры кода, в которых показано, как приложение клиента или службы использует запрашивая.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="5c7eb-110">В примере кода выполняются следующие действия для реализации публикации службы с помощью запрашивая.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="5c7eb-111">Дополнительные сведения и пример кода, который выполняет эти действия, см. в разделе [Создание точки подключения службы](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="5c7eb-112">**Создание запрашивая в каталоге при установке службы**</span><span class="sxs-lookup"><span data-stu-id="5c7eb-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="5c7eb-113">Выполните привязку к объекту компьютера для главного компьютера, на котором установлен экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="5c7eb-114">Создайте объект SCP в качестве дочернего объекта компьютера, указав начальные значения атрибутов SCP.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="5c7eb-115">Установите записи контроля доступа (ACE) в дескрипторе безопасности объекта SCP, чтобы служба изменила свойства SCP во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="5c7eb-116">Кэширование **OBJECTGUID** SCP в реестре на главном компьютере службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="5c7eb-117">Дополнительные сведения и пример кода, который выполняет эти действия, см. в разделе [Обновление точки подключения службы](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="5c7eb-118">**Обновление атрибутов SCP при запуске службы**</span><span class="sxs-lookup"><span data-stu-id="5c7eb-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="5c7eb-119">Получите **objectGUID** из реестра и используйте его для привязки к точке подключения службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="5c7eb-120">Получите атрибуты, такие как **serviceDNSName** и **СЕРВИЦЕБИНДИНГИНФОРМАТИОН**, от SCP.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="5c7eb-121">Сравните эти значения с текущими значениями и при необходимости обновите SCP.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="5c7eb-122">Дополнительные сведения и пример кода, в котором выполняются эти действия, см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="5c7eb-123">**Поиск и использование точки подключения службы с помощью клиентского приложения**</span><span class="sxs-lookup"><span data-stu-id="5c7eb-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="5c7eb-124">Выполните привязку к глобальному каталогу и выполните поиск объектов с атрибутом **keywords** , соответствующим идентификатору GUID продукта службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="5c7eb-125">Каждый найденный объект является экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="5c7eb-126">Выберите экземпляр и получите различающееся имя SCP.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="5c7eb-127">Используйте различающееся имя для привязки к SCP.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="5c7eb-128">Извлеките значения различных атрибутов из SCP, например **serviceDNSName** и **сервицебиндингинформатион**.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="5c7eb-129">Используйте эти значения для подключения к экземпляру службы и проверки его подлинности.</span><span class="sxs-lookup"><span data-stu-id="5c7eb-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="5c7eb-130">Дополнительные сведения о том, какие роли могут создавать и обновлять SCP, см. в статье [проблемы безопасности при публикации службы](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="5c7eb-131">Дополнительные сведения о том, где создать SCP, см. [в разделе Создание точки подключения службы](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="5c7eb-132">Дополнительные сведения о типе данных для хранения в SCP см. в разделе [Свойства точки подключения службы](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="5c7eb-133">Дополнительные сведения о совместной работе установщика службы и службы для поддержки текущих данных в SCP см. в разделе [Создание и обслуживание точки подключения службы](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c7eb-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




