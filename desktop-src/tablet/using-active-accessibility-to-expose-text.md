---
description: Общие сведения об использовании Active Accessibility для представления текста.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Использование Active Accessibility для представления текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701451"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="e8230-103">Использование Active Accessibility для представления текста</span><span class="sxs-lookup"><span data-stu-id="e8230-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="e8230-104">Приложения могут использовать Microsoft Active Accessibility для предоставления текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="e8230-105">Однако интерфейс [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) , определенный более ранними версиями Active Accessibility, не оптимизирован для предоставления больших объемов форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="e8230-106">Более поздние версии определяют интерфейсы, оптимизированные для предоставления больших объемов текста и текстовых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e8230-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="e8230-107">Чтобы предоставить большой объем текста, создайте отдельные объекты модели COM, поддерживающие [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)или дочерние элементы, для представления каждого выполнения текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="e8230-108">Запуск — это строка или часть строки, которая использует то же самое форматирование.</span><span class="sxs-lookup"><span data-stu-id="e8230-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="e8230-109">Active Accessibility предоставляет только текст и его расположение, но не имеет механизма для предоставления форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="e8230-110">Несмотря на эти ограничения, некоторые программы используют Active Accessibility для предоставления текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="e8230-111">Например, Microsoft Internet Explorer и Microsoft Visual Studio используют Active Accessibility для предоставления больших объемов текста.</span><span class="sxs-lookup"><span data-stu-id="e8230-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="e8230-112">Дополнительные сведения о предоставлении текста с помощью Active Accessibility см. в разделе [Специальные возможности](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="e8230-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
