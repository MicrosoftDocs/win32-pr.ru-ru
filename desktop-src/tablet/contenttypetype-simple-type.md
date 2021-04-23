---
description: Определяет тип, определяющий допустимые значения для атрибута Type \[ средства чтения журнала элемента содержимого \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Простой тип Контенттипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080942"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="c0ee7-103">Простой тип Контенттипетипе</span><span class="sxs-lookup"><span data-stu-id="c0ee7-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="c0ee7-104">Определяет тип, определяющий допустимые значения для атрибута *Type* [ \[ средства \] чтения журнала элемента содержимого](content-element--journal-reader.md).</span><span class="sxs-lookup"><span data-stu-id="c0ee7-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="c0ee7-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c0ee7-105">Patterns</span></span>

<span data-ttu-id="c0ee7-106">Простой тип **контенттипетипе** — это строка, которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="c0ee7-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="c0ee7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0ee7-107">Remarks</span></span>

<span data-ttu-id="c0ee7-108">Допустимые значения: "нормальный" и "инерт".</span><span class="sxs-lookup"><span data-stu-id="c0ee7-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="c0ee7-109">Если тип — «инерт», то содержимое, содержащееся в журнале, является страницей журнала, которая является фоном документа доступным только для чтения и не является редактируемым.</span><span class="sxs-lookup"><span data-stu-id="c0ee7-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="c0ee7-110">Это происходит при создании документа с помощью драйвера принтера составителя заметок журнала.</span><span class="sxs-lookup"><span data-stu-id="c0ee7-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ee7-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c0ee7-111">Requirements</span></span>



| <span data-ttu-id="c0ee7-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c0ee7-112">Requirement</span></span> | <span data-ttu-id="c0ee7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c0ee7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c0ee7-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0ee7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ee7-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c0ee7-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0ee7-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0ee7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ee7-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0ee7-117">None supported</span></span><br/>                                     |



 

 




