---
description: Средство записи документов XPS (Майкрософт) (МКСДВ) позволяет пользователям создавать файлы документов XPS путем печати из любого приложения Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Параметры конфигурации МКСДВ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684810"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="53464-103">Параметры конфигурации МКСДВ</span><span class="sxs-lookup"><span data-stu-id="53464-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="53464-104">Средство записи документов XPS (Майкрософт) (МКСДВ) позволяет пользователям создавать файлы документов XPS путем печати из любого приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="53464-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="53464-105">Разработчики приложений могут управлять следующими параметрами вывода МКСДВ с помощью частей PrintTicket и PrintCapabilities [схемы печати](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="53464-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="53464-106">жобинтерлеавинг</span><span class="sxs-lookup"><span data-stu-id="53464-106">JobInterleaving</span></span>

<span data-ttu-id="53464-107">Параметр Жобинтерлеавинг управляет порядком расположения содержимого для документов XPS.</span><span class="sxs-lookup"><span data-stu-id="53464-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="53464-108">Дополнительные сведения о переработе заданий см. в [спецификации XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="53464-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="53464-109">МКСДВ поддерживает следующие два параметра для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="53464-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="53464-110">**Отключено** . Этот параметр отключает вывод, чтобы все данные для каждого элемента содержимого в документе были непрерывными, что повышает эффективность произвольного доступа.</span><span class="sxs-lookup"><span data-stu-id="53464-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="53464-111">Этот вариант лучше подходит для просмотра документа XPS.</span><span class="sxs-lookup"><span data-stu-id="53464-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="53464-112">**On** — этот параметр включает вывод, чтобы данные для каждого элемента содержимого были разбиты и переупорядочены для более эффективной последовательной обработки.</span><span class="sxs-lookup"><span data-stu-id="53464-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="53464-113">Этот вариант лучше подходит для скачивания и печати через Интернет.</span><span class="sxs-lookup"><span data-stu-id="53464-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="53464-114">В следующем примере приведен пример XML-кода PrintCapabilities, который включает параметр Жобинтерлеавинг.</span><span class="sxs-lookup"><span data-stu-id="53464-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="53464-115">XML PrintTicket аналогичен, за исключением того, что он указывает конкретный параметр.</span><span class="sxs-lookup"><span data-stu-id="53464-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="53464-116">Дополнительные сведения см. в [схеме печати](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="53464-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="53464-117">Поскольку Жобинтерлеавинг не является одним из [общедоступных ключевых слов схемы печати](./print-schema-public-keywords.md), необходимо включить объявление пространства имен (в данном случае "ns0000") в теге **PrintCapabilities** (или **PrintTicket**) в начале документа PrintCapabilities (или PrintTicket), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="53464-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="53464-118">жобимажетипе</span><span class="sxs-lookup"><span data-stu-id="53464-118">JobImageType</span></span>

<span data-ttu-id="53464-119">Жобимажетипе управляет форматом вывода внедренных растровых форматов.</span><span class="sxs-lookup"><span data-stu-id="53464-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="53464-120">МКСДВ поддерживает следующие четыре параметра для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="53464-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="53464-121">**Жпегхигх** . Этот параметр указывает изображение JPEG с высоким уровнем сжатия.</span><span class="sxs-lookup"><span data-stu-id="53464-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="53464-122">Этот параметр дает минимальный размер файла, но самое низкое качество изображения.</span><span class="sxs-lookup"><span data-stu-id="53464-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="53464-123">**Жпегмед** . Этот параметр указывает изображение JPEG с средним уровнем сжатия.</span><span class="sxs-lookup"><span data-stu-id="53464-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="53464-124">Этот параметр обеспечивает оптимальный баланс размера файла и качества изображения.</span><span class="sxs-lookup"><span data-stu-id="53464-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="53464-125">**Жпеглов** . Этот параметр указывает изображение JPEG с низким уровнем сжатия.</span><span class="sxs-lookup"><span data-stu-id="53464-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="53464-126">Этот параметр приводит к наименьшему сокращению размера файла и высокого качества изображения.</span><span class="sxs-lookup"><span data-stu-id="53464-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="53464-127">**PNG** — этот параметр задает формат изображения PNG с уплотнением без потерь.</span><span class="sxs-lookup"><span data-stu-id="53464-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="53464-128">Этот параметр позволяет получить максимальный размер файла и наибольшее качество изображения.</span><span class="sxs-lookup"><span data-stu-id="53464-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="53464-129">Ниже показан XML-код PrintCapabilities параметра Жобимажетипе:</span><span class="sxs-lookup"><span data-stu-id="53464-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="53464-130">XML PrintTicket аналогичен, за исключением того, что он указывает конкретный параметр.</span><span class="sxs-lookup"><span data-stu-id="53464-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="53464-131">Дополнительные сведения см. в [схеме печати](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="53464-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="53464-132">Поскольку Жобимажетипе не является одним из [общедоступных ключевых слов схемы печати](./print-schema-public-keywords.md), необходимо включить объявление пространства имен (в данном случае "ns0000") в теге **PrintCapabilities** (или **PrintTicket**) в начале документа PrintCapabilities (или PrintTicket), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="53464-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="53464-133">См. также</span><span class="sxs-lookup"><span data-stu-id="53464-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53464-134">XPS</span><span class="sxs-lookup"><span data-stu-id="53464-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="53464-135">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="53464-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="53464-136">Схема печати</span><span class="sxs-lookup"><span data-stu-id="53464-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="53464-137">Спецификация XPS и загрузка лицензий</span><span class="sxs-lookup"><span data-stu-id="53464-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
