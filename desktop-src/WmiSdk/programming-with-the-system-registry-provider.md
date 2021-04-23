---
description: В следующих разделах описывается, как приложения могут использовать поставщик системного реестра для предоставления данных для создаваемых классов.
ms.assetid: 84604fbc-50b2-410d-84bf-4a408be26ee2
ms.tgt_platform: multiple
title: Программирование с помощью поставщика системного реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c31563a7a4ef22f1de7c4c697b201ff998a73c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898085"
---
# <a name="programming-with-the-system-registry-provider"></a><span data-ttu-id="73f1f-103">Программирование с помощью поставщика системного реестра</span><span class="sxs-lookup"><span data-stu-id="73f1f-103">Programming with the System Registry Provider</span></span>

<span data-ttu-id="73f1f-104">В следующих разделах описывается, как приложения могут использовать поставщик системного реестра для предоставления данных для создаваемых классов.</span><span class="sxs-lookup"><span data-stu-id="73f1f-104">The following topics describe how applications can use the System Registry Provider to provide data for classes that you create.</span></span>



| <span data-ttu-id="73f1f-105">Раздел</span><span class="sxs-lookup"><span data-stu-id="73f1f-105">Topic</span></span>                                                                                                                      | <span data-ttu-id="73f1f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="73f1f-106">Description</span></span>                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73f1f-107">Определение классов для поставщика системного реестра</span><span class="sxs-lookup"><span data-stu-id="73f1f-107">Defining Classes for the System Registry Provider</span></span>](defining-classes-for-the-system-registry-provider.md)                 | <span data-ttu-id="73f1f-108">Для доступа к системному реестру необходимо создать классы Windows, хранящие данные реестра в репозитории инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="73f1f-108">To access the system registry, you must create Windows classes that store registry information in the Windows Management Instrumentation (WMI) repository.</span></span>                                                                     |
| [<span data-ttu-id="73f1f-109">Использование поставщика системного реестра в качестве поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="73f1f-109">Using the System Registry Provider as a Property Provider</span></span>](using-the-system-registry-provider-as-a-property-provider.md) | <span data-ttu-id="73f1f-110">Поставщик системного реестра требует использования нескольких квалификаторов для просмотра свойств реестра.</span><span class="sxs-lookup"><span data-stu-id="73f1f-110">The System Registry Provider requires that you use several qualifiers to view registry properties.</span></span>                                                                                                                             |
| [<span data-ttu-id="73f1f-111">Описание ресурса для реестра</span><span class="sxs-lookup"><span data-stu-id="73f1f-111">Describing a Resource for the Registry</span></span>](describing-a-resource-for-the-registry.md)                                       | <span data-ttu-id="73f1f-112">Вы можете получить доступ к данным в реестре, описывающем системный ресурс.</span><span class="sxs-lookup"><span data-stu-id="73f1f-112">You can access data in the registry that describes a system resource.</span></span> <span data-ttu-id="73f1f-113">Чтобы изменить сведения, поставщику системного реестра требуется специальный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="73f1f-113">To modify the information, the System Registry Provider requires a specific syntax.</span></span>                                                                      |
| [<span data-ttu-id="73f1f-114">Доступ к неименованному значению реестра</span><span class="sxs-lookup"><span data-stu-id="73f1f-114">Accessing an Unnamed Registry Value</span></span>](accessing-an-unnamed-registry-value.md)                                             | <span data-ttu-id="73f1f-115">Чтобы получить доступ к большинству значений реестра, создайте класс для получения значений в инструментарии WMI или изучите определенные свойства реестра.</span><span class="sxs-lookup"><span data-stu-id="73f1f-115">To access most registry values, create a class to receive the values in WMI, or you can examine specific registry properties.</span></span> <span data-ttu-id="73f1f-116">Однако поставщику системного реестра требуется специальный синтаксис для просмотра неименованных значений реестра.</span><span class="sxs-lookup"><span data-stu-id="73f1f-116">However, the System Registry Provider requires a special syntax to view unnamed registry values.</span></span> |



 

 

 



