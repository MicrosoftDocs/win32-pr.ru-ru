---
title: Объект всплывающего окна
description: Объект всплывающего окна
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260545"
---
# <a name="the-balloon-object"></a><span data-ttu-id="87bd6-103">Объект всплывающего окна</span><span class="sxs-lookup"><span data-stu-id="87bd6-103">The Balloon Object</span></span>

<span data-ttu-id="87bd6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="87bd6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="87bd6-105">Microsoft Agent поддерживает текстовые субтитры метода [**говорите**](speak-method.md) , используя всплывающее слово.</span><span class="sxs-lookup"><span data-stu-id="87bd6-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="87bd6-106">Метод [**обработки**](think-method.md) позволяет отображать текст без звука в подсказке "помышления".</span><span class="sxs-lookup"><span data-stu-id="87bd6-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="87bd6-107">Начальное всплывающее окно символа по умолчанию определяется и компилируется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="87bd6-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="87bd6-108">После запуска всплывающие [**окна и свойства**](enabled-property.md) [**шрифтов**](https://www.bing.com/search?q=**Font**) могут быть переопределены пользователем.</span><span class="sxs-lookup"><span data-stu-id="87bd6-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="87bd6-109">Если пользователь изменяет свойства всплывающей подсказки слова, он влияет на все символы.</span><span class="sxs-lookup"><span data-stu-id="87bd6-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="87bd6-110">В выносках со словами « [**говорите**](speak-method.md) » и « [**думаю**](think-method.md) » для параметра размер используются одинаковые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="87bd6-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="87bd6-111">Можно получить доступ к свойствам всплывающей подсказки для символа через объект- [**выноску**](/windows/desktop/lwef/the-balloon-object) , который является дочерним по отношению к [**символьному**](/windows/desktop/lwef/the-characters-object) объекту.</span><span class="sxs-lookup"><span data-stu-id="87bd6-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="87bd6-112">Объект [**всплывающего**](/windows/desktop/lwef/the-balloon-object) объекта поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="87bd6-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="87bd6-113">**BackColor**</span><span class="sxs-lookup"><span data-stu-id="87bd6-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="87bd6-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="87bd6-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="87bd6-115">**чарсперлине**</span><span class="sxs-lookup"><span data-stu-id="87bd6-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="87bd6-116">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="87bd6-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="87bd6-117">**фонтчарсет**</span><span class="sxs-lookup"><span data-stu-id="87bd6-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="87bd6-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="87bd6-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="87bd6-119">**FontBold**</span><span class="sxs-lookup"><span data-stu-id="87bd6-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="87bd6-120">**FontItalic**</span><span class="sxs-lookup"><span data-stu-id="87bd6-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="87bd6-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="87bd6-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="87bd6-122">**фонтстрикесру**</span><span class="sxs-lookup"><span data-stu-id="87bd6-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="87bd6-123">**FontUnderline**</span><span class="sxs-lookup"><span data-stu-id="87bd6-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="87bd6-124">**ForeColor**</span><span class="sxs-lookup"><span data-stu-id="87bd6-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="87bd6-125">**нумберофлинес**</span><span class="sxs-lookup"><span data-stu-id="87bd6-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="87bd6-126">**Стиль**</span><span class="sxs-lookup"><span data-stu-id="87bd6-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="87bd6-127">**Visible**</span><span class="sxs-lookup"><span data-stu-id="87bd6-127">**Visible**</span></span>](visible-property-bal.md)

 

 