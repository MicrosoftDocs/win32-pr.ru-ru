---
description: <iconReference>Элемент указывает пользовательский значок для этой библиотеки. Этот элемент является необязательным и не имеет атрибутов или дочерних элементов.
title: Элемент Иконреференце (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997442"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="19e2b-104">Элемент Иконреференце (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="19e2b-105"><iconReference>Элемент указывает пользовательский значок для этой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="19e2b-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="19e2b-106">Этот элемент является необязательным и не имеет атрибутов или дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="19e2b-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e2b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19e2b-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="19e2b-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19e2b-108">Element Information</span></span>



| <span data-ttu-id="19e2b-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="19e2b-109">Parent Element</span></span>                                                               | <span data-ttu-id="19e2b-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="19e2b-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="19e2b-111">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="19e2b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="19e2b-112">Remarks</span></span>

<span data-ttu-id="19e2b-113">Ссылка на значок должна быть указана в форме, подходящей для функции [**паспарсеиконлокатион**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) .</span><span class="sxs-lookup"><span data-stu-id="19e2b-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="19e2b-114">Например: `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="19e2b-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19e2b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="19e2b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e2b-116">Элемент Фолдертипе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="19e2b-117">Элемент Ислибрарипиннед (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="19e2b-118">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="19e2b-119">Элемент Name (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="19e2b-120">Элемент ownerSID (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="19e2b-121">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="19e2b-122">Элемент Сеарчконнектордескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="19e2b-123">Элемент Сеарчконнектордескриптионлист (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="19e2b-124">Элемент Темплатеинфо (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="19e2b-125">Элемент Version (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="19e2b-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



