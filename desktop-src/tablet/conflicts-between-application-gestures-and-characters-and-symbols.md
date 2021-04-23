---
description: Описание конфликтов между жестами приложения и символами и символами.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Конфликты между жестами приложения и символами и символами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710865"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a><span data-ttu-id="62f4c-103">Конфликты между жестами приложения и символами и символами</span><span class="sxs-lookup"><span data-stu-id="62f4c-103">Conflicts Between Application Gestures and Characters and Symbols</span></span>

<span data-ttu-id="62f4c-104">Некоторые жесты приложения могут конфликтовать с символами, сочетаниями символов, символами, сочетаниями символов и символов или целыми словами, написанными одним росчерком.</span><span class="sxs-lookup"><span data-stu-id="62f4c-104">Some application gestures may conflict with characters, combinations of characters, symbols, combinations of characters and symbols or whole words written in a single stroke.</span></span> <span data-ttu-id="62f4c-105">Большинство этих конфликтов можно избежать, имея подробное представление о контексте, в котором выполняется жест приложения.</span><span class="sxs-lookup"><span data-stu-id="62f4c-105">Most of these conflicts are avoided by having a detailed understanding of the context in which the application gesture is performed.</span></span>

<span data-ttu-id="62f4c-106">Например, чтобы отличить правый жест от тире (-) или символа подчеркивания ( \_ ), приложение может отфильтровать, как закрывать жест с соседними символами, относительным размером по сравнению с символами или другими сведениями, содержащимися в пакете.</span><span class="sxs-lookup"><span data-stu-id="62f4c-106">For example, to distinguish a right gesture from a dash (-) or an underscore (\_), an application may filter for how close the gesture is to neighboring characters, the relative size as compared to characters, or other information contained in a packet.</span></span> <span data-ttu-id="62f4c-107">Время работы жеста приложения также может быть определяющим фактором при выборе между жестами и символами.</span><span class="sxs-lookup"><span data-stu-id="62f4c-107">The timing of the application gesture may also be a determining factor in deciding between gestures and characters.</span></span> <span data-ttu-id="62f4c-108">Перед применением жеста приложения может быть приостановка, чем перед выводом символов.</span><span class="sxs-lookup"><span data-stu-id="62f4c-108">There may be more of a pause before applying an application gesture than before inputting characters.</span></span> <span data-ttu-id="62f4c-109">Если пользователь не выполняет ряд жестов отмены или BACKSPACE, может быть несколько пауз после жеста, чем символ.</span><span class="sxs-lookup"><span data-stu-id="62f4c-109">Unless a user is performing a series of undo or backspace gestures, there may also be more of a pause after a gesture than a character.</span></span>

<span data-ttu-id="62f4c-110">Эти конфликты описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="62f4c-110">The following topics detail these conflicts:</span></span>

-   [<span data-ttu-id="62f4c-111">Конфликты с восточноазиатскими символами и символами</span><span class="sxs-lookup"><span data-stu-id="62f4c-111">Conflicts with Latin characters and symbols</span></span>](conflicts-with-latin-characters-and-symbols.md)
-   [<span data-ttu-id="62f4c-112">Конфликты с East-Asianными символами</span><span class="sxs-lookup"><span data-stu-id="62f4c-112">Conflicts with East-Asian Characters</span></span>](conflicts-with-east-asian-characters.md)

 

 



