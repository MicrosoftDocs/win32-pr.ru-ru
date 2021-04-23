---
description: Поиск компонента для активации
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Поиск компонента для активации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104560896"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="ae5e2-103">Поиск компонента для активации</span><span class="sxs-lookup"><span data-stu-id="ae5e2-103">Locating a Component for Activation</span></span>

<span data-ttu-id="ae5e2-104">Когда COM+ размещает правильную секцию — с помощью набора разделов по умолчанию, моникера секции или идентификатора секции в контексте объекта, COM + должен найти нужный компонент в этой секции.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="ae5e2-105">На следующем рисунке показано, как компонент обнаруживается и активируется, когда этот компонент находится в секции.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="ae5e2-106">Перед активацией компонента COM+ выполняет проверку, чтобы убедиться, что удостоверение пользователя, пытающееся активировать компонент, имеет права доступа к набору разделов, в котором находится компонент.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Схема, на которой показано дерево устранения неполадок для поиска компонента для активации.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="ae5e2-108">На предыдущем рисунке показано следующее.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="ae5e2-109">Если вызываемый компонент находится в секции и находится в том же приложении, что и вызывающий компонент, компонент активируется независимо от того, помечен ли вызываемый компонент как открытый или частный.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="ae5e2-110">Если вызываемый компонент находится в секции, но не существует в том же приложении, что и вызывающий компонент, COM+ проверяет, помечен ли компонент как открытый.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="ae5e2-111">Если общедоступная версия не найдена, COM+ выполняет поиск в глобальном разделе, чтобы найти общедоступную версию компонента.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="ae5e2-112">Если в глобальном разделе не обнаружена общедоступная версия компонента или если удостоверение пользователя не имеет прав на секцию, активация завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae5e2-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae5e2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ae5e2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5e2-114">Поиск секций во время активации</span><span class="sxs-lookup"><span data-stu-id="ae5e2-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



