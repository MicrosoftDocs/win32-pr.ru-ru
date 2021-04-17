---
title: БАЗОВЫЙ элемент
description: БАЗОВЫЙ элемент определяет строку URL-адреса, добавляемую к началу URL-адресов, отправляемых проигрывателю Windows Media.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- БАЗОВЫЙ элемент Windows Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698869"
---
# <a name="base-element"></a><span data-ttu-id="bb2b4-104">БАЗОВЫЙ элемент</span><span class="sxs-lookup"><span data-stu-id="bb2b4-104">BASE Element</span></span>

<span data-ttu-id="bb2b4-105">**Базовый** элемент определяет строку URL-адреса, добавляемую к началу URL-адресов, отправляемых проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="bb2b4-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bb2b4-106">Attributes</span></span>

<span data-ttu-id="bb2b4-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="bb2b4-107">**HREF** (required)</span></span>

<span data-ttu-id="bb2b4-108">Строка, добавляемая к URL-адресам, отправляемым проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="bb2b4-109">Значением по умолчанию является строка NULL ("").</span><span class="sxs-lookup"><span data-stu-id="bb2b4-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="bb2b4-110">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bb2b4-110">Parent/Child Elements</span></span>



| <span data-ttu-id="bb2b4-111">Иерархия</span><span class="sxs-lookup"><span data-stu-id="bb2b4-111">Hierarchy</span></span>       | <span data-ttu-id="bb2b4-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="bb2b4-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="bb2b4-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bb2b4-113">Parent elements</span></span> | <span data-ttu-id="bb2b4-114">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="bb2b4-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="bb2b4-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bb2b4-115">Child elements</span></span>  | <span data-ttu-id="bb2b4-116">Нет</span><span class="sxs-lookup"><span data-stu-id="bb2b4-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="bb2b4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="bb2b4-117">Remarks</span></span>

<span data-ttu-id="bb2b4-118">Этот элемент определяет строку URL-адреса, добавленную в начало URL-адреса URL, отправляемого проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="bb2b4-119">Зеркальное отображение URL-адресов — это механизм создания сценариев, который заставляет проигрыватель Windows Media открывать новый URL-адрес в браузере или кадре браузера при получении команды сценария.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="bb2b4-120">**Базовый** элемент аналогичен домашнему каталогу для относительных ссылок.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="bb2b4-121">Он влияет только на URL-адреса, отправленные с помощью команд сценария, в рамках потока содержимого, который воспроизводится проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="bb2b4-122">**Базовый** элемент, определенный как дочерний элемент элемента **ASX** , станет значением по умолчанию для всего метафайла.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="bb2b4-123">**Базовый** элемент, определенный в элементе **entry** , переопределяет любой **базовый** элемент в родительском элементе **ASX** (только для этого элемента **entry** ).</span><span class="sxs-lookup"><span data-stu-id="bb2b4-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="bb2b4-124">Если атрибут **href** не заканчивается символом/, проигрыватель Windows Media добавляет один объект в конец строки.</span><span class="sxs-lookup"><span data-stu-id="bb2b4-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bb2b4-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="bb2b4-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="bb2b4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bb2b4-126">Requirements</span></span>



| <span data-ttu-id="bb2b4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bb2b4-127">Requirement</span></span> | <span data-ttu-id="bb2b4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bb2b4-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bb2b4-129">Версия</span><span class="sxs-lookup"><span data-stu-id="bb2b4-129">Version</span></span><br/> | <span data-ttu-id="bb2b4-130">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="bb2b4-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb2b4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb2b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2b4-132">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bb2b4-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="bb2b4-133">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bb2b4-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





