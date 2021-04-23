---
description: <templateInfo>Элемент является контейнером для элемента фолдертипе, который указывает тип папки для отображения результатов запроса к этой библиотеке. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Элемент Темплатеинфо (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543098"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="c22f2-104">Элемент Темплатеинфо (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="c22f2-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="c22f2-105"><templateInfo>Элемент является контейнером для элемента [фолдертипе](schema-library-foldertype.md) , который указывает тип папки для отображения результатов запроса к этой библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c22f2-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="c22f2-106">Этот элемент является необязательным и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c22f2-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c22f2-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="c22f2-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c22f2-108">Element Information</span></span>



| <span data-ttu-id="c22f2-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c22f2-109">Parent Element</span></span>                                                               | <span data-ttu-id="c22f2-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c22f2-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="c22f2-111">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="c22f2-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="c22f2-112">Элемент Фолдертипе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="c22f2-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="c22f2-113">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="c22f2-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="c22f2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c22f2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22f2-115">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="c22f2-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="c22f2-116">[Схема описания соединителя поиска](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c22f2-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
