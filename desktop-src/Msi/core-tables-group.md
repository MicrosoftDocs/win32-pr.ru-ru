---
description: Дополнительные сведения о следующей схеме см. в разделе Условные обозначения диаграммы отношений сущностей.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Группа основных таблиц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999404"
---
# <a name="core-tables-group"></a><span data-ttu-id="1f9d5-103">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="1f9d5-103">Core Tables Group</span></span>

<span data-ttu-id="1f9d5-104">Дополнительные сведения о следующей схеме см. в разделе [Условные обозначения диаграммы отношений сущностей](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d5-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![Группа основных таблиц](images/core.png)

<span data-ttu-id="1f9d5-106">Основная группа состоит из таблиц, описывающих фундаментальные функции и компоненты приложения и пакета установщика.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="1f9d5-107">Поэтому разработчикам пакетов установки следует подумать о том, как заполнить эти таблицы первыми, поскольку Организация большей части базы данных станет очевидной из содержимого этой группы.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="1f9d5-108">В [таблице Feature](feature-table.md) перечислены все компоненты, принадлежащие приложению.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="1f9d5-109">[Таблица условий](condition-table.md) содержит условные выражения, которые определяют, будет ли установлен определенный компонент.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="1f9d5-110">В [таблице феатурекомпонентс](featurecomponents-table.md) описано, какие компоненты относятся к каждому компоненту.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="1f9d5-111">В [таблице Component](component-table.md) перечислены все компоненты, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="1f9d5-112">В [таблице Directory](directory-table.md) перечислены каталоги, которые необходимы во время установки.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="1f9d5-113">Поскольку каждый компонент должен быть связан с одним и только одним каталогом, таблица Component тесно связана с этой таблицей и имеет внешний ключ к таблице Directory.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="1f9d5-114">В [таблице публишкомпонент](publishcomponent-table.md) перечислены компоненты и компоненты, опубликованные для использования другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="1f9d5-115">[Компоненты и компоненты](components-and-features.md) — это два типа объявлений компонентов.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="1f9d5-116">В [таблице мсиассембли](msiassembly-table.md) указаны параметры установщик Windows для платформа .NET Framework сборок среды CLR и сборок Win32.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="1f9d5-117">В [таблице мсиассемблинаме](msiassemblyname-table.md) указана схема для элементов строгого имени кэша сборок для среды CLR или сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="1f9d5-118">[Таблица ComPlus](complus-table.md) содержит сведения, необходимые для установки приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="1f9d5-119">[Таблица исолатедкомпонент](isolatedcomponent-table.md) связывает компонент, указанный в \_ столбце "приложение-компонент" (обычно это exe-файл), с компонентом, указанным в \_ общем столбце Component (обычно это общая библиотека DLL).</span><span class="sxs-lookup"><span data-stu-id="1f9d5-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="1f9d5-120">[Таблица обновления](upgrade-table.md) содержит сведения, необходимые при [значительных обновлениях](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d5-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



