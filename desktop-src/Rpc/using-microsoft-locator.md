---
title: Использование локатора Майкрософт
description: Служба "Локатор Майкрософт" является службой имен по умолчанию. Библиотека времени выполнения RPC использует ее для поиска серверных программ на системах узлов сервера.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Удаленный вызов процедур RPC, задачи, использование локатора Майкрософт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888372"
---
# <a name="using-microsoft-locator"></a><span data-ttu-id="199b9-105">Использование локатора Майкрософт</span><span class="sxs-lookup"><span data-stu-id="199b9-105">Using Microsoft Locator</span></span>

<span data-ttu-id="199b9-106">Служба "Локатор Майкрософт" является службой имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="199b9-106">Microsoft Locator is the default name service.</span></span> <span data-ttu-id="199b9-107">Библиотека времени выполнения RPC использует ее для поиска серверных программ на системах узлов сервера.</span><span class="sxs-lookup"><span data-stu-id="199b9-107">The RPC run-time library uses it to find server programs on server host systems.</span></span>

<span data-ttu-id="199b9-108">**Примечание**    . Указатель Microsoft RPC не поддерживается в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="199b9-108">**Note**  Microsoft RPC locator is not supported in Windows Vista and later operating systems.</span></span>

<span data-ttu-id="199b9-109">До Windows 2000 локатор Майкрософт не предоставил записей службы постоянных имен.</span><span class="sxs-lookup"><span data-stu-id="199b9-109">Prior to Windows 2000, Microsoft Locator did not provide persistent name service entries.</span></span> <span data-ttu-id="199b9-110">Все записи в службе имен хранились в кэше памяти на главном компьютере серверной программы.</span><span class="sxs-lookup"><span data-stu-id="199b9-110">All entries in the name service were stored in a memory cache on the server program's host computer.</span></span> <span data-ttu-id="199b9-111">Указатель использовал механизм вещания для обнаружения расположения серверов по запросу клиентов.</span><span class="sxs-lookup"><span data-stu-id="199b9-111">The locator used a broadcast mechanism to discover the location of servers as requested by clients.</span></span> <span data-ttu-id="199b9-112">При завершении работы системы узла все записи службы имен теряются.</span><span class="sxs-lookup"><span data-stu-id="199b9-112">Whenever the host system shut down, all name service entries were lost.</span></span>

<span data-ttu-id="199b9-113">Начиная с выпуска Windows 2000 локатор Майкрософт теперь поддерживает записи службы постоянных имен.</span><span class="sxs-lookup"><span data-stu-id="199b9-113">Beginning with the release of Windows 2000, Microsoft Locator now supports persistent name service entries.</span></span> <span data-ttu-id="199b9-114">Для этого система использует распределенную службу каталогов для хранения записей службы имен.</span><span class="sxs-lookup"><span data-stu-id="199b9-114">To accomplish this, the system employs a distributed directory service to store name service entries.</span></span> <span data-ttu-id="199b9-115">Этот механизм имеет несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="199b9-115">This mechanism has several advantages:</span></span>

-   <span data-ttu-id="199b9-116">**Сохраняемости.**</span><span class="sxs-lookup"><span data-stu-id="199b9-116">**Persistence.**</span></span> <span data-ttu-id="199b9-117">Серверным программам больше не требуется экспортировать сведения о привязке в службу имен при каждом запуске.</span><span class="sxs-lookup"><span data-stu-id="199b9-117">Server programs are no longer required to export their binding information to the name service each time they start up.</span></span> <span data-ttu-id="199b9-118">Служба имен теперь хранит информацию до тех пор, пока серверная программа на сетевом администраторе не удалит ее явным образом.</span><span class="sxs-lookup"><span data-stu-id="199b9-118">The name service now stores the information until the server program on the network administrator explicitly removes it.</span></span>
-   <span data-ttu-id="199b9-119">**Мощности.**</span><span class="sxs-lookup"><span data-stu-id="199b9-119">**Efficiency.**</span></span> <span data-ttu-id="199b9-120">Устраняя большую часть широковещательной рассылки для записей службы имен, локатор сокращает сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="199b9-120">By eliminating the majority of broadcasting for name service entries, the locator reduces network traffic.</span></span> <span data-ttu-id="199b9-121">Он также находит записи службы имен быстрее.</span><span class="sxs-lookup"><span data-stu-id="199b9-121">It also finds name service entries more rapidly.</span></span>
-   <span data-ttu-id="199b9-122">**Взаимодействие между доменами.**</span><span class="sxs-lookup"><span data-stu-id="199b9-122">**Cross-Domain Interoperability.**</span></span> <span data-ttu-id="199b9-123">Теперь клиенты могут выполнять запросы службы имен в нескольких доменах.</span><span class="sxs-lookup"><span data-stu-id="199b9-123">Clients are now able to make name service requests across multiple domains.</span></span>

<span data-ttu-id="199b9-124">Текущие версии локатора Майкрософт имеют обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="199b9-124">Current versions of Microsoft Locator are backward compatible.</span></span> <span data-ttu-id="199b9-125">Например, хост-система сервера, на котором работает локатор, поставляемая с Windows 2000, может правильно работать в сети, содержащей серверные системы, на которых выполняется локатор, входящий в состав Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="199b9-125">For instance, a server host system running the locator that ships with Windows 2000 can operate correctly on a network that contains server host systems running the locator that ships with Windows NT 4.0.</span></span>

<span data-ttu-id="199b9-126">В выпуске Windows 2000 локатор Майкрософт теперь поддерживает записи службы имен для групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="199b9-126">With the release of Windows 2000, Microsoft Locator now supports name service entries for groups of users.</span></span> <span data-ttu-id="199b9-127">Кроме того, он позволяет создавать профили пользователей.</span><span class="sxs-lookup"><span data-stu-id="199b9-127">It also provides the ability for you to create user profiles.</span></span>

<span data-ttu-id="199b9-128">Кроме того, текущая версия локатора Майкрософт поддерживает использование списков управления доступом в записях службы имен.</span><span class="sxs-lookup"><span data-stu-id="199b9-128">In addition, the current version of Microsoft Locator supports the use of Access Control Lists in name service entries.</span></span> <span data-ttu-id="199b9-129">Эта возможность повышает безопасность сети.</span><span class="sxs-lookup"><span data-stu-id="199b9-129">This ability enhances the security of the network.</span></span>

<span data-ttu-id="199b9-130">Поддержка самонастраивающийся теперь включена в указатель Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="199b9-130">Plug and Play support is now included in Microsoft Locator.</span></span> <span data-ttu-id="199b9-131">Таким образом, он может прозрачно выполнять обработку самонастраивающийся событий, таких как изменение домена.</span><span class="sxs-lookup"><span data-stu-id="199b9-131">Therefore, it can transparently handle Plug and Play events such as domain changes.</span></span> <span data-ttu-id="199b9-132">Дополнительные сведения см. в разделе [**рпкнсбиндинжекспортпнп**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) и [**рпкнсбиндингунекспортпнп**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span><span class="sxs-lookup"><span data-stu-id="199b9-132">For more information, see [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) and [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span></span>

 

 




