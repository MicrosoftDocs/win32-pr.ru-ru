---
title: Использование интерфейса Идиректорйобжект
description: При создании клиента ADSI на языке C или C++, который использует раннее связывание, вы получите более широкий спектр типов данных ADSI, доступных для использования в клиенте, если он вызывает интерфейс Идиректорйобжект, а не интерфейс IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- Идиректорйобжект ADSI, использование
- ADSI ADSI, использование с помощью интерфейса Идиректорйобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772893"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="bb805-105">Использование интерфейса Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="bb805-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="bb805-106">При создании клиента ADSI на языке C или C++, который использует раннее связывание, вы получите более широкий спектр типов данных ADSI, доступных для использования в клиенте, если он вызывает интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) , а не интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="bb805-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="bb805-107">Интерфейс **идиректорйобжект** предоставляет методы для поддержки подмножества свойств обслуживания объекта и для доступа к его атрибутам.</span><span class="sxs-lookup"><span data-stu-id="bb805-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="bb805-108">На следующем рисунке показаны связи между структурами данных.</span><span class="sxs-lookup"><span data-stu-id="bb805-108">The following figure shows the relationships among the data structures.</span></span>

![структуры данных интерфейса идиректорйобжект](images/ds2dso.png)

<span data-ttu-id="bb805-110">На предыдущем рисунке в [**\_ \_ сведениях об объекте структуры ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) определяются свойства, которые определяют объект по различающемся имени, относительное различающееся имя, по контейнеру (парентдн), по типу объекта (классдн) и по определению схемы (счемадн).</span><span class="sxs-lookup"><span data-stu-id="bb805-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="bb805-111">[**\_ \_ Сведения о**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) атрибутах attr дескриптора атрибута состоят из имени, типа данных, массива значений данных, показанного в [**адсвалуе**](/windows/desktop/api/Iads/ns-iads-adsvalue), и флага, направляющего базовую службу каталогов для выполнения определенных операций с атрибутами, подробно описанными в таблице [объявления \_ attr \_ \*](adsi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bb805-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="bb805-112">Типы данных этих атрибутов включают расширенные типы синтаксиса ADSI, которые подробно описаны в [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum).</span><span class="sxs-lookup"><span data-stu-id="bb805-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




