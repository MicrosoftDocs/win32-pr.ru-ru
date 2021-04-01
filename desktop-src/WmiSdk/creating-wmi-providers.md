---
description: Разработчики могут расширить инфраструктуру WMI, разрабатывая поставщики WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Создание поставщиков WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081601"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="93e97-103">Создание поставщиков WMI</span><span class="sxs-lookup"><span data-stu-id="93e97-103">Creating WMI Providers</span></span>

<span data-ttu-id="93e97-104">Разработчики могут расширить инфраструктуру WMI, разрабатывая поставщики WMI.</span><span class="sxs-lookup"><span data-stu-id="93e97-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="93e97-105">Поставщики WMI — это COM-объекты, реализующие указанный набор интерфейсов, и до последнего времени они всегда были реализованы в C++.</span><span class="sxs-lookup"><span data-stu-id="93e97-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="93e97-106">Теперь можно использовать управляемые языки, например C#, для реализации поставщиков WMI.</span><span class="sxs-lookup"><span data-stu-id="93e97-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="93e97-107">В версии 3,5 платформы .NET Framework появилась платформа расширений поставщика WMI, которая делает это возможным.</span><span class="sxs-lookup"><span data-stu-id="93e97-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="93e97-108">Дополнительные сведения о создании поставщиков WMI с помощью этой платформы см. в статье [Создание связанных поставщиков WMI с помощью расширения поставщика WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="93e97-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="93e97-109">Вы также можете создать поставщик с помощью инфраструктуры управления Windows (MI), версии следующего поколения WMI.</span><span class="sxs-lookup"><span data-stu-id="93e97-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="93e97-110">Дополнительные сведения см. [в разделе Реализация поставщика MI](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="93e97-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="93e97-111">В следующей таблице приводится описание содержимого этого раздела.</span><span class="sxs-lookup"><span data-stu-id="93e97-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="93e97-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="93e97-112">Topic</span></span>                                                      | <span data-ttu-id="93e97-113">Описание</span><span class="sxs-lookup"><span data-stu-id="93e97-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="93e97-114">Предоставление данных инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="93e97-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="93e97-115">Содержит общие сведения о шагах, связанных с созданием поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="93e97-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="93e97-116">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="93e97-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="93e97-117">Описывает задачи, которые необходимо выполнить при создании различных типов поставщиков WMI.</span><span class="sxs-lookup"><span data-stu-id="93e97-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
