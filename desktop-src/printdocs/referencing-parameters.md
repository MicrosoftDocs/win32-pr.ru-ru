---
description: Сведения о ссылках на параметры и элемент Параметердеф. Примером параметра, включающего элемент ParameterRef, является пользовательский параметр размера носителя.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Создание ссылок на параметры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405327"
---
# <a name="referencing-parameters"></a><span data-ttu-id="454a9-104">Создание ссылок на параметры</span><span class="sxs-lookup"><span data-stu-id="454a9-104">Referencing Parameters</span></span>

<span data-ttu-id="454a9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="454a9-105">This topic is not current.</span></span> <span data-ttu-id="454a9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="454a9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="454a9-107">Конкретный пример параметра, включающего элемент ParameterRef, — это пользовательский параметр размера носителя.</span><span class="sxs-lookup"><span data-stu-id="454a9-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="454a9-108">Обратите внимание, что он ссылается на два параметра: Пажемедиасиземедиасизевидс и Пажемедиасиземедиасизехеигхт.</span><span class="sxs-lookup"><span data-stu-id="454a9-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="454a9-109">Каждый экземпляр ParameterRef ссылается на экземпляр Параметердеф, который определен в любом расположении документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="454a9-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="454a9-110">Дополнительные сведения об элементе Параметердеф см. в разделе [параметердеф](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="454a9-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="454a9-111">Основные сведения об определении параметров см. в разделе [элементы параметердеф и параметеринит](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="454a9-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="454a9-112">Просто создать параметризованный параметр недостаточно, чтобы убедиться, что параметр будет обрабатываться и обрабатываться правильно.</span><span class="sxs-lookup"><span data-stu-id="454a9-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="454a9-113">Поставщик PrintCapabilities/PrintTicket и клиенты должны предоставить дополнительную поддержку для правильной реализации параметризованных экземпляров параметров.</span><span class="sxs-lookup"><span data-stu-id="454a9-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="454a9-114">Необходимые поведения описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="454a9-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="454a9-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="454a9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="454a9-116">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="454a9-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



