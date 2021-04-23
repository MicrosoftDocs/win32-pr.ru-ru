---
title: Ошибка роли контейнера ARIA
description: Ошибка роли контейнера ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- ариаконтаинерролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986784"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="cecff-104">Ошибка роли контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="cecff-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="cecff-105">Текст</span><span class="sxs-lookup"><span data-stu-id="cecff-105">Text</span></span>

<span data-ttu-id="cecff-106">Элемент с определенным " **Active-Descendants** " не имеет роли контейнера (**ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **дерево**, **контекстное**, **таблист**, **строка**).</span><span class="sxs-lookup"><span data-stu-id="cecff-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="cecff-107">Тип</span><span class="sxs-lookup"><span data-stu-id="cecff-107">Type</span></span>

<span data-ttu-id="cecff-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cecff-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="cecff-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cecff-109">Description</span></span>

<span data-ttu-id="cecff-110">Эта ошибка применяется к элементам, имеющим атрибут **ARIA-активедесцендант** .</span><span class="sxs-lookup"><span data-stu-id="cecff-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="cecff-111">Элемент выглядит как контейнер с установленным атрибутом **ARIA-активедесцендант** , но атрибут Role элемента не имеет значения, допустимого для контейнера.</span><span class="sxs-lookup"><span data-stu-id="cecff-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="cecff-112">Чтобы устранить эту ошибку, установите атрибут **Role** в качестве значения роли "веб-приложения со специальными возможностями" (ожидать-ARIA), допустимого для элемента контейнера: **ComboBox**, **Grid**, **ListBox**, **меню**, **MenuBar**, **RadioGroup**, **таблист**, **Tree** или **контекстное**.</span><span class="sxs-lookup"><span data-stu-id="cecff-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="cecff-113">Пример</span><span class="sxs-lookup"><span data-stu-id="cecff-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="cecff-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cecff-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cecff-115">Ошибка роли ARIA</span><span class="sxs-lookup"><span data-stu-id="cecff-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




