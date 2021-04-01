---
description: Секции по умолчанию
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Секции по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262765"
---
# <a name="default-partitions"></a><span data-ttu-id="ce207-103">Секции по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ce207-103">Default Partitions</span></span>

<span data-ttu-id="ce207-104">Когда пользователю назначается секция по умолчанию, COM+ сначала пытается активировать компоненты в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ce207-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="ce207-105">В случае сбоя активации COM+ выполняет поиск компонента для активации в глобальном разделе.</span><span class="sxs-lookup"><span data-stu-id="ce207-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="ce207-106">Исключением из этого процесса является ситуация, когда компонент COM+ включает моникер секции, который явно указывает секцию, в которой находится компонент.</span><span class="sxs-lookup"><span data-stu-id="ce207-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="ce207-107">В этом случае моникер раздела имеет приоритет над любой конфигурацией секции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce207-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="ce207-108">При использовании локальных секций раздел по умолчанию назначается пользователям с помощью папки " **Пользователи раздела COM+** " в средстве администрирования "службы компонентов" на сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="ce207-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="ce207-109">При использовании наборов разделов в Active Directory Секция по умолчанию пользователя определяется набором разделов пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce207-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce207-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ce207-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce207-111">Локальные секции</span><span class="sxs-lookup"><span data-stu-id="ce207-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="ce207-112">Свойства секции</span><span class="sxs-lookup"><span data-stu-id="ce207-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="ce207-113">Секции и Active Directory</span><span class="sxs-lookup"><span data-stu-id="ce207-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="ce207-114">Глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="ce207-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



