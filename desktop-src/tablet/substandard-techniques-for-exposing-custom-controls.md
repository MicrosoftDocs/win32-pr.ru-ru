---
description: Описание методов для предоставления пользовательских элементов управления.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Методы для предоставления настраиваемых элементов управления с подстандартом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674095"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="7a319-103">Методы для предоставления настраиваемых элементов управления с подстандартом</span><span class="sxs-lookup"><span data-stu-id="7a319-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="7a319-104">Если приложение не поддерживает Microsoft Active Accessibility, оно может быть не полностью доступно.</span><span class="sxs-lookup"><span data-stu-id="7a319-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="7a319-105">Следующие методы визуализируют элементы управления с частичным уровнем совместимости:</span><span class="sxs-lookup"><span data-stu-id="7a319-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="7a319-106">Возврат описательной строки при запросе элемента управления с помощью \_ сообщения WM GetText.</span><span class="sxs-lookup"><span data-stu-id="7a319-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="7a319-107">Например, можно разрешить пользовательскому эквиваленту элемента управления "Кнопка", помеченного как "Печать", вернуть строку "Кнопка" Печать ".</span><span class="sxs-lookup"><span data-stu-id="7a319-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="7a319-108">Он определяет как тип элемента управления, так и метку.</span><span class="sxs-lookup"><span data-stu-id="7a319-108">This identifies both control type and label.</span></span> <span data-ttu-id="7a319-109">Одна и та же строка подходит для кнопки с меткой, отличной от текстовой, такой как изображение принтера.</span><span class="sxs-lookup"><span data-stu-id="7a319-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="7a319-110">Аналогичным образом, можно разрешить настраиваемому элементу управления, который ведет себя как флажок, чтобы возвратить строку заголовка "флажок" печать включена "установленным.</span><span class="sxs-lookup"><span data-stu-id="7a319-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="7a319-111">Поддержка сообщения WM \_ жетдлгкоде, определяющего поддерживаемый ввод с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="7a319-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="7a319-112">Например, можно разрешить пользовательскому эквиваленту элемента управления "поле ввода" обрабатывать WM \_ жетдлгкоде, возвращая длгк \_ хассетсел, если он обрабатывает сообщения для установки выделения, длгк \_ вантарровс, если он использует клавиши со стрелками, и длгк \_ вантчарс, чтобы указать, что он использует символьные данные.</span><span class="sxs-lookup"><span data-stu-id="7a319-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="7a319-113">Только элементы управления, имеющие собственные дескрипторы окна, могут отвечать на \_ сообщения WM gettext и WM \_ жетдлгкоде.</span><span class="sxs-lookup"><span data-stu-id="7a319-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="7a319-114">Во избежание проблем совместимости с вспомогательными средствами следует следовать рекомендациям Active Accessibility в тесном проектировании пользовательских элементов управления.</span><span class="sxs-lookup"><span data-stu-id="7a319-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="7a319-115">Дополнительные сведения о том, как избежать проблем совместимости с вспомогательными средствами, см. в разделе [Специальные возможности](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="7a319-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
