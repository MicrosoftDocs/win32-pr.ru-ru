---
description: Существует несколько функций, изменяющих установку компонентов продукта и компонентов. Ниже описано, как изменить компоненты и компоненты.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Работа с функциями и компонентами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673929"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="1b585-104">Работа с функциями и компонентами</span><span class="sxs-lookup"><span data-stu-id="1b585-104">Working with Features and Components</span></span>

<span data-ttu-id="1b585-105">Существует несколько функций, изменяющих установку компонентов продукта [и](components-and-features.md)компонентов.</span><span class="sxs-lookup"><span data-stu-id="1b585-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="1b585-106">Ниже описано, как изменить компоненты и компоненты.</span><span class="sxs-lookup"><span data-stu-id="1b585-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="1b585-107">**Изменение установки компонентов и компонентов**</span><span class="sxs-lookup"><span data-stu-id="1b585-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="1b585-108">Задайте уровень установки компонента или компонента, вызвав функцию [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .</span><span class="sxs-lookup"><span data-stu-id="1b585-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="1b585-109">Каждому компоненту пакета назначается уровень установки в [таблице Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b585-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="1b585-110">Если уровень установки компонента ниже уровня, установленного параметром [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), этот компонент выбирается для установки.</span><span class="sxs-lookup"><span data-stu-id="1b585-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="1b585-111">После вызова **мсисетинсталллевел** можно явно изменить, установлен ли компонент.</span><span class="sxs-lookup"><span data-stu-id="1b585-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="1b585-112">Определите, какие состояния доступны для указанного компонента, вызвав функцию [**мсижетфеатуревалидстатес**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .</span><span class="sxs-lookup"><span data-stu-id="1b585-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="1b585-113">Получите требования к месту на диске для указанного компонента и его дочерних компонентов, вызвав функцию [**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .</span><span class="sxs-lookup"><span data-stu-id="1b585-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="1b585-114">Получите текущее состояние компонента или компонента, вызвав функцию [**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) или функцию [**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="1b585-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="1b585-115">Измените состояние компонента или компонента с помощью функции [**мсисетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) или функции [**мсисеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="1b585-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



