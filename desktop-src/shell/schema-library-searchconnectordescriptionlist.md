---
description: Этот <searchConnectorDescriptionList> элемент содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку. Каждый соединитель поиска определяется <searchConnectorDescription> элементом. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Элемент Сеарчконнектордескриптионлист (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985892"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="f2ece-105">Элемент Сеарчконнектордескриптионлист (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="f2ece-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="f2ece-106">Этот <searchConnectorDescriptionList> элемент содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку.</span><span class="sxs-lookup"><span data-stu-id="f2ece-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="f2ece-107">Каждый соединитель поиска определяется <searchConnectorDescription> элементом.</span><span class="sxs-lookup"><span data-stu-id="f2ece-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="f2ece-108">Этот элемент является необязательным и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f2ece-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ece-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2ece-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="f2ece-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f2ece-110">Element Information</span></span>



| <span data-ttu-id="f2ece-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f2ece-111">Parent Element</span></span>                                                               | <span data-ttu-id="f2ece-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f2ece-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2ece-113">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="f2ece-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="f2ece-114">Элемент Сеарчконнектордескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="f2ece-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="f2ece-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2ece-115">Remarks</span></span>

<span data-ttu-id="f2ece-116">Соединители поиска для федеративного поиска Windows и области обработчика протокола не могут быть добавлены в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="f2ece-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2ece-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f2ece-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2ece-118">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="f2ece-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="f2ece-119">[Схема описания соединителя поиска](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2ece-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
