---
title: Переводы языка COM
description: Компоненты, созданные с помощью модели COM, можно повторно использовать в приложениях, написанных на любом языке программирования, поддерживающем COM. Это обусловлено тем, что COM является двоичным стандартом и, как таковой, не зависит от языка.
ms.assetid: 89e74768-b7bd-4ab6-9129-9e677a9c14ca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f622b83b998402e82d6cf20975331645362c55e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410624"
---
# <a name="com-language-translations"></a><span data-ttu-id="441c3-104">Переводы языка COM</span><span class="sxs-lookup"><span data-stu-id="441c3-104">COM Language Translations</span></span>

<span data-ttu-id="441c3-105">Компоненты, созданные с помощью модели COM, можно повторно использовать в приложениях, написанных на любом языке программирования, поддерживающем COM.</span><span class="sxs-lookup"><span data-stu-id="441c3-105">Components created using the Component Object Model (COM) can be reused in applications written in any programming language that supports COM.</span></span> <span data-ttu-id="441c3-106">Это обусловлено тем, что COM является двоичным стандартом и, как таковой, не зависит от языка.</span><span class="sxs-lookup"><span data-stu-id="441c3-106">This is because COM is a binary standard and, as such, is language-independent.</span></span>

<span data-ttu-id="441c3-107">Объекты COM описаны в наиболее соответствующем языке программирования или языках.</span><span class="sxs-lookup"><span data-stu-id="441c3-107">COM objects are documented in the most relevant programming language or languages.</span></span> <span data-ttu-id="441c3-108">Например, объекты, создаваемые для использования на веб-страницах, обычно задокументированы в системе разработки Microsoft Visual Basic, тогда как объекты уровня системы обычно документируются в C++.</span><span class="sxs-lookup"><span data-stu-id="441c3-108">For example, objects that are created for use in webpages are typically documented in the Microsoft Visual Basic development system, whereas system-level objects are typically documented in C++.</span></span> <span data-ttu-id="441c3-109">Однако, поскольку модель COM не зависит от языка, вы не ограничены использованием объекта на том же языке, на котором он написан или документирован.</span><span class="sxs-lookup"><span data-stu-id="441c3-109">However, because COM is language-neutral, you are not limited to using an object in the same language in which it is written or documented.</span></span> <span data-ttu-id="441c3-110">Например, можно написать приложение в JScript, использующее элемент управления, созданный в C++ и описанный в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="441c3-110">For example, you can write an application in JScript that uses a control created in C++ and documented in Visual Basic.</span></span>

<span data-ttu-id="441c3-111">В следующих разделах рассматриваются различия между языками программирования и описывается способ преобразования синтаксиса объектов COM с одного языка на другой.</span><span class="sxs-lookup"><span data-stu-id="441c3-111">The following topics discuss the differences between programming languages and describe how to translate COM object syntax from one language to another.</span></span> <span data-ttu-id="441c3-112">В дополнительных разделах описывается использование COM-объектов в различных языках и средах сценариев.</span><span class="sxs-lookup"><span data-stu-id="441c3-112">Additional topics describe how to use COM objects in various scripting languages and environments.</span></span>

-   [<span data-ttu-id="441c3-113">Синтаксические отличия</span><span class="sxs-lookup"><span data-stu-id="441c3-113">Syntax Differences</span></span>](syntax-differences.md)
-   [<span data-ttu-id="441c3-114">Преобразования типов данных</span><span class="sxs-lookup"><span data-stu-id="441c3-114">Data Type Conversions</span></span>](data-type-conversions.md)
-   [<span data-ttu-id="441c3-115">IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="441c3-115">IDL Files</span></span>](idl-files.md)
-   [<span data-ttu-id="441c3-116">Преобразование синтаксиса COM-объектов для языков программирования</span><span class="sxs-lookup"><span data-stu-id="441c3-116">Translating COM Object Syntax for Programming Languages</span></span>](translating-com-object-syntax-for-programming-languages.md)
-   [<span data-ttu-id="441c3-117">Создание сценариев с помощью COM-объектов</span><span class="sxs-lookup"><span data-stu-id="441c3-117">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)

<span data-ttu-id="441c3-118">Цель — решить наиболее распространенные проблемы преобразования языка, возникающие при использовании COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="441c3-118">The intent is to address the most common language translation issues that arise when using COM objects.</span></span> <span data-ttu-id="441c3-119">Описанные методики и принципы применимы к любому языку программирования или сценарию, поддерживающему COM.</span><span class="sxs-lookup"><span data-stu-id="441c3-119">The techniques and principles described apply to any programming or scripting language that supports COM.</span></span> <span data-ttu-id="441c3-120">Поскольку языки сценариев и языки программирования представляют разные парадигмы программирования, преобразование между языками сценариев и языками программирования не устраняется.</span><span class="sxs-lookup"><span data-stu-id="441c3-120">Because scripting languages and programming languages represent different programming paradigms, translation between scripting languages and programming languages is not addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="441c3-121">См. также</span><span class="sxs-lookup"><span data-stu-id="441c3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="441c3-122">Модель COM</span><span class="sxs-lookup"><span data-stu-id="441c3-122">Component Object Model (COM)</span></span>](component-object-model--com--portal.md)
</dt> </dl>

 

 




