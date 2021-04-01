---
title: Каноническая XML
description: Канонический XML решает проблему преобразования набора узлов XML в байты таким образом, что тривиальные изменения в XML (например, изменение порядка атрибутов в элементе) не изменяют итоговую форму Byte.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Веб-службы канонического XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891252"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="c379a-106">Каноническая XML</span><span class="sxs-lookup"><span data-stu-id="c379a-106">XML Canonicalization</span></span>

<span data-ttu-id="c379a-107">Канонический XML решает проблему преобразования набора узлов XML в байты таким образом, что тривиальные изменения в XML (например, изменение порядка атрибутов в элементе) не изменяют итоговую форму Byte.</span><span class="sxs-lookup"><span data-stu-id="c379a-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="c379a-108">Байты, полученные из канонической разбора, обычно используются для создания криптографической подписи поверх XML-содержимого.</span><span class="sxs-lookup"><span data-stu-id="c379a-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="c379a-109">Часто используемые алгоритмы канонизации XML стандартизируют следующие аспекты:</span><span class="sxs-lookup"><span data-stu-id="c379a-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="c379a-110">Кодировка символов (UTF-8 без преамбулы)</span><span class="sxs-lookup"><span data-stu-id="c379a-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="c379a-111">Символы перевода строки и другие формы символов</span><span class="sxs-lookup"><span data-stu-id="c379a-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="c379a-112">Порядок атрибутов в элементе</span><span class="sxs-lookup"><span data-stu-id="c379a-112">Attribute order in an element</span></span>
-   <span data-ttu-id="c379a-113">Форма пустого элемента</span><span class="sxs-lookup"><span data-stu-id="c379a-113">Empty element form</span></span>
-   <span data-ttu-id="c379a-114">Подготовка к просмотру объявлений пространств имен</span><span class="sxs-lookup"><span data-stu-id="c379a-114">Rendering namespace declarations</span></span>

<span data-ttu-id="c379a-115">API-интерфейсы [**всстартреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) и [**всендреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) предоставляют функцию канонизации XML при чтении документа.</span><span class="sxs-lookup"><span data-stu-id="c379a-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="c379a-116">API-интерфейсы [**всстартвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) и [**всендвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) предоставляют функцию канонизации XML при записи документа.</span><span class="sxs-lookup"><span data-stu-id="c379a-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="c379a-117">Для канонизации используются следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="c379a-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="c379a-118">**\_ \_ алгоритм КАНОНИЗАЦИИ XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="c379a-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="c379a-119">**\_ \_ \_ идентификатор свойства WS-канонизации \_**</span><span class="sxs-lookup"><span data-stu-id="c379a-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="c379a-120">Для канонизации используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c379a-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="c379a-121">**всендреадерканоникализатион**</span><span class="sxs-lookup"><span data-stu-id="c379a-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="c379a-122">**всендвритерканоникализатион**</span><span class="sxs-lookup"><span data-stu-id="c379a-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="c379a-123">**всстартреадерканоникализатион**</span><span class="sxs-lookup"><span data-stu-id="c379a-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="c379a-124">**всстартвритерканоникализатион**</span><span class="sxs-lookup"><span data-stu-id="c379a-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="c379a-125">Для канонизации используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="c379a-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="c379a-126">**\_ \_ \_ Инклюзивные \_ префиксы WS-XML**</span><span class="sxs-lookup"><span data-stu-id="c379a-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="c379a-127">**\_свойство WS-XML \_ канонизации \_**</span><span class="sxs-lookup"><span data-stu-id="c379a-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




