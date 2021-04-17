---
title: Ошибка роли ARIA
description: Ошибка роли ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- ариаролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105681708"
---
# <a name="aria-role-error"></a><span data-ttu-id="aff0d-104">Ошибка роли ARIA</span><span class="sxs-lookup"><span data-stu-id="aff0d-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="aff0d-105">Текст</span><span class="sxs-lookup"><span data-stu-id="aff0d-105">Text</span></span>

<span data-ttu-id="aff0d-106">Элемент имеет недопустимую роль ожидать-ARIA.</span><span class="sxs-lookup"><span data-stu-id="aff0d-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="aff0d-107">Тип</span><span class="sxs-lookup"><span data-stu-id="aff0d-107">Type</span></span>

<span data-ttu-id="aff0d-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="aff0d-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="aff0d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aff0d-109">Description</span></span>

<span data-ttu-id="aff0d-110">Эта ошибка применяется ко всем элементам, имеющим атрибут [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) .</span><span class="sxs-lookup"><span data-stu-id="aff0d-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="aff0d-111">Он указывает, что атрибут **Role** не является допустимым значением роли "веб-приложения со специальными возможностями" (ожидать-ARIA), доступным в соответствии со спецификацией ожидать-ARIA.</span><span class="sxs-lookup"><span data-stu-id="aff0d-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="aff0d-112">Задание допустимой роли позволяет убедиться, что элемент правильно интерпретируется программами чтения с экрана и другими средствами вспомогательных технологий.</span><span class="sxs-lookup"><span data-stu-id="aff0d-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="aff0d-113">Чтобы устранить эту ошибку, присвойте атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) допустимое значение роли ожидать-ARIA.</span><span class="sxs-lookup"><span data-stu-id="aff0d-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="aff0d-114">Обратите внимание, что абстрактные роли ожидать-ARIA недопустимы.</span><span class="sxs-lookup"><span data-stu-id="aff0d-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="aff0d-115">Пример</span><span class="sxs-lookup"><span data-stu-id="aff0d-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="aff0d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="aff0d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff0d-117">Ошибка роли контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="aff0d-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




