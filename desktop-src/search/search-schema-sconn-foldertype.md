---
description: <folderType>Элемент указывает идентификатор GUID для папки типа. Этот элемент обязателен, если <templateInfo> элемент существует. У него нет атрибутов и дочерних элементов.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Элемент Фолдертипе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497055"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="44477-105">Элемент Фолдертипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="44477-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="44477-106"><folderType>Элемент указывает идентификатор GUID для папки типа.</span><span class="sxs-lookup"><span data-stu-id="44477-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="44477-107">Этот элемент обязателен, если <templateInfo> элемент существует.</span><span class="sxs-lookup"><span data-stu-id="44477-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="44477-108">У него нет атрибутов и дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="44477-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="44477-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44477-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="44477-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="44477-110">Element Information</span></span>



| <span data-ttu-id="44477-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="44477-111">Parent Element</span></span>                                                                         | <span data-ttu-id="44477-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="44477-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="44477-113">Элемент Темплатеинфо (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="44477-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="44477-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44477-114">Remarks</span></span>

<span data-ttu-id="44477-115">GUID по умолчанию — {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, общий тип папки для соединителей федеративного поиска (OpenSearch Search).</span><span class="sxs-lookup"><span data-stu-id="44477-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="44477-116">Пример элемента Фолдертипе</span><span class="sxs-lookup"><span data-stu-id="44477-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



