---
description: Поставщик представления является экземпляром и поставщиком метода, который создает новые классы на основе экземпляров других классов.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Просмотр поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911480"
---
# <a name="view-provider"></a><span data-ttu-id="b5df7-103">Просмотр поставщика</span><span class="sxs-lookup"><span data-stu-id="b5df7-103">View Provider</span></span>

<span data-ttu-id="b5df7-104">Поставщик представления является экземпляром и поставщиком метода, который создает новые классы на основе экземпляров других классов.</span><span class="sxs-lookup"><span data-stu-id="b5df7-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="b5df7-105">Поставщик представлений можно использовать для получения свойств из различных исходных классов, разных пространств имен или различных компьютеров и объединения свойств в виде одного класса.</span><span class="sxs-lookup"><span data-stu-id="b5df7-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="b5df7-106">Как экземпляр и поставщик метода, поставщик представления поддерживает стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и следующие методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="b5df7-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="b5df7-107">**креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="b5df7-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="b5df7-108">**ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="b5df7-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="b5df7-109">**ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="b5df7-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="b5df7-110">**жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="b5df7-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="b5df7-111">**путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="b5df7-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="b5df7-112">Дополнительные сведения об квалификаторах, используемых для определения классов поставщиков представления, см. в разделе [квалификаторы, относящиеся к поставщику представления](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b5df7-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="b5df7-113">Дополнительные сведения о представлениях см. в разделе [связывание классов вместе](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="b5df7-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="b5df7-114">На 64-разрядных платформах доступны две версии поставщика представления.</span><span class="sxs-lookup"><span data-stu-id="b5df7-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="b5df7-115">Дополнительные сведения см. в разделе [Получение и предоставление данных на 64-разрядном компьютере](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b5df7-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="b5df7-116">Поставщик представления реализуется в ViewProv.dll.</span><span class="sxs-lookup"><span data-stu-id="b5df7-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5df7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b5df7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5df7-118">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="b5df7-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



