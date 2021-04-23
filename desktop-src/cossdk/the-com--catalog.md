---
description: В каталоге COM+ хранятся атрибуты приложения COM+, атрибуты классов и атрибуты уровня компьютера. Он гарантирует согласованность между этими атрибутами и предоставляет общие операции над этими атрибутами.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Каталог COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662077"
---
# <a name="the-com-catalog"></a><span data-ttu-id="dff30-104">Каталог COM+</span><span class="sxs-lookup"><span data-stu-id="dff30-104">The COM+ Catalog</span></span>

<span data-ttu-id="dff30-105">В каталоге COM+ хранятся атрибуты приложения COM+, атрибуты классов и атрибуты уровня компьютера.</span><span class="sxs-lookup"><span data-stu-id="dff30-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="dff30-106">Он гарантирует согласованность между этими атрибутами и предоставляет общие операции над этими атрибутами.</span><span class="sxs-lookup"><span data-stu-id="dff30-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="dff30-107">Каталог COM+ использует два разных хранилища, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="dff30-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="dff30-108">База данных регистрации COM+</span><span class="sxs-lookup"><span data-stu-id="dff30-108">The COM+ registration database</span></span>
-   <span data-ttu-id="dff30-109">Реестр Windows (**\_ \_ корневой класс классов hKey**)</span><span class="sxs-lookup"><span data-stu-id="dff30-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="dff30-110">Каталог представляет единое логическое представление этих двух магазинов и предоставляет их через библиотеку администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="dff30-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="dff30-111">Эта библиотека предоставляет, используя язык сценариев, все функциональные возможности средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="dff30-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="dff30-112">Для существующих COM-компонентов, которые не нуждаются в новых службах COM+, поиск выполняется в существующем реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="dff30-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="dff30-113">Каталог COM+ также использует реестр Windows для регистрации библиотеки типов и прокси-сервера интерфейса или заглушки.</span><span class="sxs-lookup"><span data-stu-id="dff30-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="dff30-114">Регистрация разбиения</span><span class="sxs-lookup"><span data-stu-id="dff30-114">Split Registration</span></span>

<span data-ttu-id="dff30-115">Для новых компонентов, которые уже являются существующими COM-компонентами, которые используются в среде служб (например, компоненты MTS), основной COM-аспект регистрации хранится в реестре Windows, а новые службы и атрибуты (например, компоненты в очереди) хранятся в базе данных регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="dff30-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="dff30-116">Такая *Регистрация называется разделенной регистрацией*.</span><span class="sxs-lookup"><span data-stu-id="dff30-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="dff30-117">Каждый атрибут хранится только в одном расположении: в реестре Windows или в базе данных регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="dff30-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="dff30-118">Новые COM-компоненты регистрируются исключительно в базе данных регистрации COM+, что приводит к дублированию в реестре Windows, чтобы существующие средства могли их использовать.</span><span class="sxs-lookup"><span data-stu-id="dff30-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="dff30-119">Обновления транзакций каталога</span><span class="sxs-lookup"><span data-stu-id="dff30-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="dff30-120">Некоторые операции с каталогом выполняются в транзакционном режиме.</span><span class="sxs-lookup"><span data-stu-id="dff30-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="dff30-121">При вызове библиотеки администрирования COM+ из транзакционного компонента обновления базы данных регистрации COM+ будут выполняться в пределах границ транзакции вызывающего компонента.</span><span class="sxs-lookup"><span data-stu-id="dff30-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="dff30-122">Однако обновления, затрагивающие изменения в других хранилищах (например, файловую систему и реестр Windows), не обязательно будут полностью транзакционными.</span><span class="sxs-lookup"><span data-stu-id="dff30-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="dff30-123">Прерванная транзакция может оставить эти магазины в состоянии, которое не согласуется с изменениями, внесенными в друг друга или в базу данных регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="dff30-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dff30-124">См. также</span><span class="sxs-lookup"><span data-stu-id="dff30-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dff30-125">Создание пакетов установки для приложений COM+</span><span class="sxs-lookup"><span data-stu-id="dff30-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="dff30-126">Развертывание прокси приложения</span><span class="sxs-lookup"><span data-stu-id="dff30-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="dff30-127">Служебная программа репликации COMREPL</span><span class="sxs-lookup"><span data-stu-id="dff30-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



