---
description: Можно указать, какие параметры установки доступны пользователям и приложениям для выбора путем создания таблицы компонентов и таблицы компонентов.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Управление состояниями выбора компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272468"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="5d481-103">Управление состояниями выбора компонентов</span><span class="sxs-lookup"><span data-stu-id="5d481-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="5d481-104">Можно указать, какие параметры установки доступны пользователям и приложениям для выбора путем создания [таблицы компонентов](feature-table.md) и [таблицы компонентов](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d481-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="5d481-105">Чтобы предотвратить выбор состояния объявления для функции, включите **мсидбфеатуреаттрибутесдисалловадвертисе** в поле атрибуты функции в [таблице Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d481-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="5d481-106">Чтобы предотвратить выбор состояния "Запуск из источника" или "Запуск из сети" для функции, включите **мсидбкомпонентаттрибутеслокалонли** в поля Attributes в [таблице Component](component-table.md) для каждого компонента, принадлежащего этой функции.</span><span class="sxs-lookup"><span data-stu-id="5d481-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="5d481-107">Если у функции нет компонентов, она всегда имеет доступ к параметрам "запустить с исходного кода" и "выполнить с моего компьютера".</span><span class="sxs-lookup"><span data-stu-id="5d481-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="5d481-108">Чтобы предотвратить выбор состояния запуска от моего компьютера для функции, включите **мсидбкомпонентаттрибутессаурцеонли** в поля атрибуты [таблицы Component](component-table.md) для каждого компонента, принадлежащего этой функции.</span><span class="sxs-lookup"><span data-stu-id="5d481-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="5d481-109">Если у функции нет компонентов, она всегда имеет доступ к параметрам "запустить с исходного кода" и "выполнить с моего компьютера".</span><span class="sxs-lookup"><span data-stu-id="5d481-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="5d481-110">Новые дочерние функции могут быть созданы путем включения **мсидбфеатуреаттрибутесфолловпарент** и **Мсидбфеатуреаттрибутесуидисалловабсент** в поле Attributes [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d481-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



