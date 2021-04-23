---
description: Установщик Windows сохраняет все сведения об установке в реляционной базе данных. Вы можете изменить эту базу данных и, следовательно, установить ее с помощью преобразований и слияний.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Слияния и преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651152"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="75db5-104">Слияния и преобразования</span><span class="sxs-lookup"><span data-stu-id="75db5-104">Merges and Transforms</span></span>

<span data-ttu-id="75db5-105">Установщик Windows сохраняет все сведения об установке в реляционной базе данных.</span><span class="sxs-lookup"><span data-stu-id="75db5-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="75db5-106">Вы можете изменить эту базу данных и, следовательно, установить ее с помощью преобразований и слияний.</span><span class="sxs-lookup"><span data-stu-id="75db5-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="75db5-107">Преобразования</span><span class="sxs-lookup"><span data-stu-id="75db5-107">Transforms</span></span>

<span data-ttu-id="75db5-108">[Преобразование базы данных](database-transforms.md) добавляет или заменяет элементы в исходной базе данных.</span><span class="sxs-lookup"><span data-stu-id="75db5-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="75db5-109">Например, преобразование может изменить весь текст в пользовательском интерфейсе приложения с французского на английский.</span><span class="sxs-lookup"><span data-stu-id="75db5-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="75db5-110">К основным применениям преобразований относятся:</span><span class="sxs-lookup"><span data-stu-id="75db5-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="75db5-111">Настройка базовых пакетов установки для определенных групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="75db5-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="75db5-112">Преобразования можно использовать для инкапсуляции различных настроек одного базового пакета, которые необходимы разным группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="75db5-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="75db5-113">Например, это полезно в организациях, где отделы поддержки финансов и штатного отдела нуждаются в различных установках определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="75db5-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="75db5-114">Базовый пакет продукта может быть доступен всем пользователям в одной административной точке установки с соответствующими настройками, распространяемыми в каждую группу пользователей отдельно.</span><span class="sxs-lookup"><span data-stu-id="75db5-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="75db5-115">Синхронизация приложений на разных языках.</span><span class="sxs-lookup"><span data-stu-id="75db5-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="75db5-116">Преобразования полезны для хранения пакетов, созданных в широко разделенных расположениях, синхронизируемых во время разработки.</span><span class="sxs-lookup"><span data-stu-id="75db5-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="75db5-117">Например, если обновление впервые разрабатывается для английской версии приложения, имеющегося на английском и французском языках, преобразование можно применить к обновленной версии на английском языке, которая преобразует ее в обновленную версию для французского языка.</span><span class="sxs-lookup"><span data-stu-id="75db5-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="75db5-118">К базовому пакету можно применить несколько преобразований, а затем применить их во время установки.</span><span class="sxs-lookup"><span data-stu-id="75db5-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="75db5-119">Это расширяет возможности установщика для создания пользовательских пакетов и предоставляет механизм для эффективного назначения наиболее подходящих установок разным группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="75db5-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="75db5-120">Установка исправлений приложений.</span><span class="sxs-lookup"><span data-stu-id="75db5-120">Patching applications.</span></span>

    <span data-ttu-id="75db5-121">Преобразования можно использовать для применения незначительного исправления в приложении, которое не гарантирует существенного обновления.</span><span class="sxs-lookup"><span data-stu-id="75db5-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="75db5-122">Дополнительные сведения об исправлениях см. в разделе [пакеты исправлений](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="75db5-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="75db5-123">Слияния</span><span class="sxs-lookup"><span data-stu-id="75db5-123">Merges</span></span>

<span data-ttu-id="75db5-124">Слияние объединяет две базы данных в одну базу данных и добавляет, а не заменяет информацию.</span><span class="sxs-lookup"><span data-stu-id="75db5-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="75db5-125">Если одни и те же сведения существуют в обеих базах данных, возникает конфликт слияния.</span><span class="sxs-lookup"><span data-stu-id="75db5-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="75db5-126">Слияние полезно для групп разработчиков, так как они позволяют разделить большое приложение на части, которые можно будет объединить позже.</span><span class="sxs-lookup"><span data-stu-id="75db5-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="75db5-127">Например, элементы базы данных для установки нового компонента можно разрабатывать отдельно, а затем объединить в основную базу данных установки.</span><span class="sxs-lookup"><span data-stu-id="75db5-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="75db5-128">Дополнительные сведения см. в разделе [модули слияния](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="75db5-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="75db5-129">Команда разработчиков может применить операцию слияния следующим образом:</span><span class="sxs-lookup"><span data-stu-id="75db5-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="75db5-130">Разделяйте группы и одновременно работайте с различными компонентами большого приложения.</span><span class="sxs-lookup"><span data-stu-id="75db5-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="75db5-131">Каждая группа разработки затем заполняет базу данных сведениями об установке для своего собственного компонента, не заботясь о других компонентах приложения.</span><span class="sxs-lookup"><span data-stu-id="75db5-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="75db5-132">После завершения разработки компонента базу данных этого компонента можно объединить в основную базу данных установки для всего приложения.</span><span class="sxs-lookup"><span data-stu-id="75db5-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



