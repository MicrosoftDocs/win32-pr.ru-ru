---
title: иттсбуфнотифисинкв
description: иттсбуфнотифисинкв
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986778"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="15e19-103">иттсбуфнотифисинкв</span><span class="sxs-lookup"><span data-stu-id="15e19-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="15e19-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15e19-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="15e19-105">Обработчик должен вызвать через **закладку**.</span><span class="sxs-lookup"><span data-stu-id="15e19-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="15e19-106">Во время предварительной обработки речевого вывода код Microsoft Agent вставляет закладки между словами и применяет получение этих закладок для появления шага текста в окне всплывающей программы.</span><span class="sxs-lookup"><span data-stu-id="15e19-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="15e19-107">Хотя SAPI не требует чего-либо больше, чем появления этих закладок в течение некоторого времени до окончания utterance, закладки должны возвращаться в относительно своевременном режиме поддержки Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15e19-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="15e19-108">Обратите внимание, что в некоторых языках, например на японском языке, не существует определенного понятия «Word».</span><span class="sxs-lookup"><span data-stu-id="15e19-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="15e19-109">Метод [**говорите**](speak-method.md) от Microsoft Agent определяет слово как подключенную строку символов, которая имеет значение и произношение в изоляции.</span><span class="sxs-lookup"><span data-stu-id="15e19-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="15e19-110">Microsoft Agent использует довольно простой код синтаксического анализа для определения того, что такое слово: Поиск символов, разделенных пробелом.</span><span class="sxs-lookup"><span data-stu-id="15e19-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="15e19-111">Таким образом, в английской строке "The 101 Далматианс": "," 101 "и" Далматианс "есть три слова.</span><span class="sxs-lookup"><span data-stu-id="15e19-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="15e19-112">Текст, включенный в тег Microsoft Agent Map, рассматривается в целях отображения как единое слово.</span><span class="sxs-lookup"><span data-stu-id="15e19-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




