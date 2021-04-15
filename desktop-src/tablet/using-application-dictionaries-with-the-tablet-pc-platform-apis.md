---
description: Чтобы использовать словарь приложений с API Tablet PC, сначала необходимо создать файл со списком слов для словаря приложения.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Использование словарей приложений с интерфейсами API платформы Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682656"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="3bdaa-103">Использование словарей приложений с интерфейсами API платформы Tablet PC</span><span class="sxs-lookup"><span data-stu-id="3bdaa-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="3bdaa-104">Чтобы использовать словарь приложений с API Tablet PC, сначала необходимо создать файл со списком слов для словаря приложения.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="3bdaa-105">Самым простым решением для этого является использование текстового файла, содержащего список слов.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="3bdaa-106">Когда приложение загрузится, оно считывает текстовый файл и [**создает объект списка слов в**](inkwordlist-class.md) файле.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="3bdaa-107">Для каждого [**рекогнизерконтекст**](inkrecognizercontext-class.md) , связанного с словарем приложения, задайте для свойства список [**слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта **рекогнизерконтекст** значение List в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="3bdaa-108">В следующем примере показано, как создать объект [**список слов**](inkwordlist-class.md) из коллекции [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="3bdaa-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="3bdaa-109">В этом примере предполагается, что вы уже загрузили список слов с диска и создали коллекцию StringCollection из этих слов.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> <span data-ttu-id="3bdaa-110">Чтобы задать свойство " [**список слов**](inkwordlist-class.md) ", свойство [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="3bdaa-111">Если свойство [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) не пусто, выдается исключение.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="3bdaa-112">Кроме того, слова не должны добавляться в список слов после того, как они были назначены объекту **рекогнизерконтекст** .</span><span class="sxs-lookup"><span data-stu-id="3bdaa-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="3bdaa-113">Слова, добавляемые в список слов после его назначения объекту **рекогнизерконтекст** , не обновляются в распознавателе.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="3bdaa-114">Чтобы обновить список слов, необходимо переназначить объект **списка слов** свойству списка [**слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта **рекогнизерконтекст** .</span><span class="sxs-lookup"><span data-stu-id="3bdaa-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="3bdaa-115">Чтобы получить максимальную точность распознавания, объедините фактоидс с словарем приложения в отношении выгод.</span><span class="sxs-lookup"><span data-stu-id="3bdaa-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="3bdaa-116">Дополнительные сведения о связи между фактоидс и словарями приложений см. в разделе [Основные сведения о списках слов, контексте распознавателя и фактоидс](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="3bdaa-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="3bdaa-117">Пример использования словарей приложений с элементом управления [InkEdit](inkedit-control-reference.md) см. в разделе [Использование словаря приложения с InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="3bdaa-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
