---
title: Co-Branding Интернет-магазинов
description: Co-Branding Интернет-магазинов
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Интернет-магазины проигрывателя Windows Media, фирменная символика
- Интернет-магазины, совместное добавление фирменной символики
- Тип 1 Интернет-магазины, софирменная символика
- Тип 2 Интернет-магазинов, фирменная символика
- Совместное фирменная символика Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691216"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="8ad1b-108">Co-Branding Интернет-магазинов</span><span class="sxs-lookup"><span data-stu-id="8ad1b-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="8ad1b-109">Производители персональных компьютеров, не работающие с музыкальным магазином, могут использовать фирменную символику с поставщиками Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="8ad1b-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="8ad1b-110">Программа установки проигрывателя Windows Media поддерживает параметр командной строки Сервицеекстра, позволяющий изготовителям оборудования задавать настраиваемый атрибут, который Интернет-магазин может использовать для указания того, какой поставщик оборудования установил первоначальное Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="8ad1b-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="8ad1b-111">Например, если изготовитель компьютера с именем Fabrikam хочет установить в качестве начального Интернет-магазина Proseware музыкальное хранилище, для установки проигрывателя Windows Media 10 может использоваться следующая командная строка:</span><span class="sxs-lookup"><span data-stu-id="8ad1b-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="8ad1b-112">Когда проигрыватель Windows Media устанавливается таким образом, проигрыватель добавляет строку Сервицеекстра каждый раз при открытии службы proseware.</span><span class="sxs-lookup"><span data-stu-id="8ad1b-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="8ad1b-113">В следующем примере показан URL-адрес, который проигрыватель Windows Media отправит в службу Proseware для получения документа ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="8ad1b-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="8ad1b-114">В Proseware Online Store можно использовать строку запроса, чтобы определить, какой изготовитель оборудования установил Windows Media Player, и возвратить динамически созданный документ ServiceInfo, указывающий на фирменную версию Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="8ad1b-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ad1b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad1b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad1b-116">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8ad1b-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8ad1b-117">**Параметры командной строки программы установки для Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8ad1b-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




