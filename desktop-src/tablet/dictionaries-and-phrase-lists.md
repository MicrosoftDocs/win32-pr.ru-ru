---
description: Словарь или список возможных слов, используемых в языковой модели конкретного распознавателя, содержится в одном или нескольких словарях.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Словари и списки фраз
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693470"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="6aa85-103">Словари и списки фраз</span><span class="sxs-lookup"><span data-stu-id="6aa85-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="6aa85-104">Словарь или список возможных слов, используемых в языковой модели конкретного распознавателя, содержится в одном или нескольких словарях.</span><span class="sxs-lookup"><span data-stu-id="6aa85-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="6aa85-105">Распознаватель выполняет поиск во всех словарях, доступных в системе при компиляции совпадений распознавания.</span><span class="sxs-lookup"><span data-stu-id="6aa85-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="6aa85-106">Для изменения некоторых из этих словарей можно использовать Microsoft Speech API (SAPI).</span><span class="sxs-lookup"><span data-stu-id="6aa85-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="6aa85-107">Список фраз предоставляет еще одно средство изменения словаря распознавателя.</span><span class="sxs-lookup"><span data-stu-id="6aa85-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="6aa85-108">Добавление слов в список фраз расширяет словарь; Добавление слов и последующее ограничение распознавателя на использование только списка фраз (в отличие от списка фраз и словарей) ограничивает словарь.</span><span class="sxs-lookup"><span data-stu-id="6aa85-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="6aa85-109">Предыдущие выпуски API технологии планшетных ПК основывались на концепции списков слов.</span><span class="sxs-lookup"><span data-stu-id="6aa85-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="6aa85-110">Списки слов практически идентичны спискам фраз и используются для той же цели при работе непосредственно с объектом [**рекогнизерконтекст**](inkrecognizercontext-class.md) в приложении, для которого включена поддержка рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6aa85-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="6aa85-111">Дополнительные сведения о том, где и когда следует использовать списки слов, см. в разделе [Настройка контекста для элементов управления Ink-Enabled](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6aa85-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="6aa85-112">Если размер списка, к которому нужно расширить лексикон, превышает 100 000 слов, рекомендуется использовать словарь вместо списка слов или список фраз.</span><span class="sxs-lookup"><span data-stu-id="6aa85-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



