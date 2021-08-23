---
description: Чтобы использовать словарь приложений с API Tablet PC, сначала необходимо создать файл со списком слов для словаря приложения.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Использование словарей приложений с интерфейсами API платформы Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c30fec5539a9b1f4efb0ca89a53568becff2368942d069149106a4032676d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091321"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Использование словарей приложений с интерфейсами API платформы Tablet PC

Чтобы использовать словарь приложений с API Tablet PC, сначала необходимо создать файл со списком слов для словаря приложения.

Самым простым решением для этого является использование текстового файла, содержащего список слов. Когда приложение загрузится, оно считывает текстовый файл и [**создает объект списка слов в**](inkwordlist-class.md) файле. Для каждого [**рекогнизерконтекст**](inkrecognizercontext-class.md) , связанного с словарем приложения, задайте для свойства список [**слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта **рекогнизерконтекст** значение List в текстовом файле.

В следующем примере показано, как создать объект [**список слов**](inkwordlist-class.md) из коллекции [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) . В этом примере предполагается, что вы уже загрузили список слов с диска и создали коллекцию StringCollection из этих слов.


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
> Чтобы задать свойство " [**список слов**](inkwordlist-class.md) ", свойство [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) должно быть пустым. Если свойство [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) не пусто, выдается исключение. Кроме того, слова не должны добавляться в список слов после того, как они были назначены объекту **рекогнизерконтекст** . Слова, добавляемые в список слов после его назначения объекту **рекогнизерконтекст** , не обновляются в распознавателе. Чтобы обновить список слов, необходимо переназначить объект **списка слов** свойству списка [**слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта **рекогнизерконтекст** .

 

Чтобы получить максимальную точность распознавания, объедините фактоидс с словарем приложения в отношении выгод. Дополнительные сведения о связи между фактоидс и словарями приложений см. в разделе [Основные сведения о списках слов, контексте распознавателя и фактоидс](understanding-wordlists--the-recognizercontext--and-factoids.md).

Пример использования словарей приложений с элементом управления [InkEdit](inkedit-control-reference.md) см. в разделе [Использование словаря приложения с InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
