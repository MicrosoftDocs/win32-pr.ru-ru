---
description: <folderType>Элемент указывает идентификатор GUID для типа папки. Этот элемент обязателен <templateInfo> , если элемент существует, в противном случае — необязательный. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
title: Элемент Фолдертипе (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984589"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="833c5-105">Элемент Фолдертипе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="833c5-106"><folderType>Элемент указывает идентификатор GUID для типа папки.</span><span class="sxs-lookup"><span data-stu-id="833c5-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="833c5-107">Этот элемент обязателен <templateInfo> , если элемент существует, в противном случае — необязательный.</span><span class="sxs-lookup"><span data-stu-id="833c5-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="833c5-108">Этот элемент не имеет атрибутов и не содержит дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="833c5-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="833c5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="833c5-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="833c5-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="833c5-110">Element Information</span></span>



| <span data-ttu-id="833c5-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="833c5-111">Parent Element</span></span>                                                           | <span data-ttu-id="833c5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="833c5-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="833c5-113">Элемент Темплатеинфо (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="833c5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="833c5-114">Remarks</span></span>

<span data-ttu-id="833c5-115">Задание типа папки определяет столбцы и сведения, отображаемые в проводнике Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="833c5-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="833c5-116">Идентификаторы типов папок ([**фолдертипеид**](foldertypeid.md)) являются идентификаторами GUID, определенными в шлгуид. h.</span><span class="sxs-lookup"><span data-stu-id="833c5-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="833c5-117">В следующей таблице перечислены идентификаторы GUID общих типов папок.</span><span class="sxs-lookup"><span data-stu-id="833c5-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="833c5-118">Тип папки</span><span class="sxs-lookup"><span data-stu-id="833c5-118">Folder Type</span></span>      | <span data-ttu-id="833c5-119">Код GUID</span><span class="sxs-lookup"><span data-stu-id="833c5-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="833c5-120">Универсальная библиотека</span><span class="sxs-lookup"><span data-stu-id="833c5-120">Generic Library</span></span>  | <span data-ttu-id="833c5-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="833c5-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="833c5-122">Библиотеки пользователей</span><span class="sxs-lookup"><span data-stu-id="833c5-122">Users Libraries</span></span>  | <span data-ttu-id="833c5-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="833c5-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="833c5-124">Папка документов</span><span class="sxs-lookup"><span data-stu-id="833c5-124">Documents Folder</span></span> | <span data-ttu-id="833c5-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="833c5-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="833c5-126">Папка "рисунки"</span><span class="sxs-lookup"><span data-stu-id="833c5-126">Pictures Folder</span></span>  | <span data-ttu-id="833c5-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="833c5-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="833c5-128">Папка "видео"</span><span class="sxs-lookup"><span data-stu-id="833c5-128">Videos Folder</span></span>    | <span data-ttu-id="833c5-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="833c5-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="833c5-130">Папка "игры"</span><span class="sxs-lookup"><span data-stu-id="833c5-130">Games Folder</span></span>     | <span data-ttu-id="833c5-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="833c5-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="833c5-132">Папка "Музыка"</span><span class="sxs-lookup"><span data-stu-id="833c5-132">Music Folder</span></span>     | <span data-ttu-id="833c5-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="833c5-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="833c5-134">Контакты</span><span class="sxs-lookup"><span data-stu-id="833c5-134">Contacts</span></span>         | <span data-ttu-id="833c5-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="833c5-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="833c5-136">См. также</span><span class="sxs-lookup"><span data-stu-id="833c5-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="833c5-137">Элемент Иконреференце (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="833c5-138">Элемент Ислибрарипиннед (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="833c5-139">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="833c5-140">Элемент Name (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="833c5-141">Элемент ownerSID (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="833c5-142">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="833c5-143">Элемент Сеарчконнектордескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="833c5-144">Элемент Сеарчконнектордескриптионлист (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="833c5-145">Элемент Темплатеинфо (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="833c5-146">Элемент Version (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="833c5-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



