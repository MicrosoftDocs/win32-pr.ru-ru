---
description: Международный вывод текста
ms.assetid: e6cc5169-1a6e-40f8-b616-e76ec919195c
title: Международный вывод текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8ba7eb6f1a043bb642945e178f3545bcd51738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081401"
---
# <a name="international-text-display"></a><span data-ttu-id="4c6ab-103">Международный вывод текста</span><span class="sxs-lookup"><span data-stu-id="4c6ab-103">International Text Display</span></span>

<span data-ttu-id="4c6ab-104">Существует четыре возможных варианта отображения международного текста, что также влечет за собой вывод сложных наборов символов:</span><span class="sxs-lookup"><span data-stu-id="4c6ab-104">There are four possible options for displaying international text, which also entails the output of complex scripts:</span></span>

-   <span data-ttu-id="4c6ab-105">Вызов API текста Windows</span><span class="sxs-lookup"><span data-stu-id="4c6ab-105">Calling Windows text APIs</span></span>
-   <span data-ttu-id="4c6ab-106">Создание экземпляра стандартных элементов управления "изменение" Windows</span><span class="sxs-lookup"><span data-stu-id="4c6ab-106">Instantiating Windows standard edit controls</span></span>
-   <span data-ttu-id="4c6ab-107">Создание экземпляров элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="4c6ab-107">Instantiating rich edit controls</span></span>
-   <span data-ttu-id="4c6ab-108">Вызов Uniscribe</span><span class="sxs-lookup"><span data-stu-id="4c6ab-108">Calling Uniscribe</span></span>

<span data-ttu-id="4c6ab-109">Описание и преимущества каждого из этих параметров см. в разделе [Параметры отображения текста](https://msdn.microsoft.com/globalization/mt662335) .</span><span class="sxs-lookup"><span data-stu-id="4c6ab-109">Please see [Options for Displaying Text](https://msdn.microsoft.com/globalization/mt662335) for the explanation and advantages of each of these options.</span></span> <span data-ttu-id="4c6ab-110">Затем вы решаете выбрать оптимальный вариант для вашего приложения, основываясь на сложности приложения и его функциях проектирования.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-110">It is then up to you to decide which is the best option for your application, based on the application's complexity and its design features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c6ab-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4c6ab-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6ab-112">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-112">**TextOut**</span></span>](/windows/win32/api/wingdi/nf-wingdi-textouta)
</dt> <dt>

[<span data-ttu-id="4c6ab-113">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-113">**ExtTextOut**</span></span>](/windows/win32/api/wingdi/nf-wingdi-exttextouta)
</dt> <dt>

[<span data-ttu-id="4c6ab-114">**таббедтекстаут**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-114">**TabbedTextOut**</span></span>](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)
</dt> <dt>

[<span data-ttu-id="4c6ab-115">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-115">**DrawText**</span></span>](/windows/win32/api/winuser/nf-winuser-drawtext)
</dt> <dt>

[<span data-ttu-id="4c6ab-116">**жеттаббедтекстекстент**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-116">**GetTabbedTextExtent**</span></span>](/windows/win32/api/winuser/nf-winuser-gettabbedtextextenta)
</dt> <dt>

[<span data-ttu-id="4c6ab-117">**GetTextExtentPoint32**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-117">**GetTextExtentPoint32**</span></span>](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)
</dt> <dt>

[<span data-ttu-id="4c6ab-118">**жеттекстекстентекспоинт**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-118">**GetTextExtentExPoint**</span></span>](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)
</dt> <dt>

[<span data-ttu-id="4c6ab-119">**Элемент управления "Поле ввода"**</span><span class="sxs-lookup"><span data-stu-id="4c6ab-119">**Edit control**</span></span>](../msi/edit-control.md)
</dt> <dt>

[<span data-ttu-id="4c6ab-120">Расширенное редактирование</span><span class="sxs-lookup"><span data-stu-id="4c6ab-120">Rich Edit</span></span>](../controls/about-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="4c6ab-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="4c6ab-121">Uniscribe</span></span>](uniscribe.md)
</dt> </dl>

 

 
