---
description: Чтобы создать словарь приложений, необходимо задать свойство «список слов» объекта Рекогнизерконтекст.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Использование словаря приложения с InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc919fc071f249611d42b8decb6ce4fb0b0f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662388"
---
# <a name="using-an-application-dictionary-with-inkedit"></a><span data-ttu-id="732b9-103">Использование словаря приложения с InkEdit</span><span class="sxs-lookup"><span data-stu-id="732b9-103">Using an Application Dictionary with InkEdit</span></span>

<span data-ttu-id="732b9-104">Чтобы создать словарь приложений, необходимо задать свойство « [**список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) » объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="732b9-104">To create an application dictionary, it is necessary to set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="732b9-105">Элемент управления [InkEdit](inkedit-control-reference.md) не предоставляет объект **рекогнизерконтекст** , поэтому невозможно напрямую задать свойство " **список слов** " объекта **рекогнизерконтекст** элемента управления InkEdit.</span><span class="sxs-lookup"><span data-stu-id="732b9-105">The [InkEdit](inkedit-control-reference.md) control does not expose the **RecognizerContext** object, so it is not possible to directly set the **WordList** property of the InkEdit control's **RecognizerContext** object.</span></span>

<span data-ttu-id="732b9-106">Чтобы использовать словарь приложения с элементом управления [InkEdit](inkedit-control-reference.md) , необходимо взять штрихи за пределами элемента управления InkEdit, передать их в новый объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) со свойством " [**список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) ", для которого задано значение " [**список слов**](inkwordlist-class.md) ", содержащий словарь приложения, сохранить результаты из этого объекта **рекогнизерконтекст** , а затем передать результаты обратно в элемент управления InkEdit.</span><span class="sxs-lookup"><span data-stu-id="732b9-106">To use an application dictionary with an [InkEdit](inkedit-control-reference.md) control, you must take the strokes out of the InkEdit control, pass them to a new [**RecognizerContext**](inkrecognizercontext-class.md) object with the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property set to a [**WordList**](inkwordlist-class.md) containing the application dictionary, store the results from this **RecognizerContext** object, and then pass the results back to the InkEdit control.</span></span>

## <a name="example"></a><span data-ttu-id="732b9-107">Пример</span><span class="sxs-lookup"><span data-stu-id="732b9-107">Example</span></span>

<span data-ttu-id="732b9-108">В следующем коде на языке C \# показан пример этой методики.</span><span class="sxs-lookup"><span data-stu-id="732b9-108">The following C\# code shows an example of this technique.</span></span>


```C++
private RecognizerContext rc;
private WordList wl;
private int wlSelStart;
private int wlSelLen;
private bool isRecoPending = false;

private void Form1_Load(object sender, EventArgs e)
{
  //event handlers must be attached for dictionary to work.
  inkEdit1.Recognition += new Microsoft.Ink.InkEditRecognitionEventHandler(inkEdit1_Recognition);
  inkEdit1.TextChanged += new EventHandler(inkEdit1_TextChanged);

  //create a WordList that contains the application dictionary
  wl = new WordList();
  //...
  //Add dictionary terms to the WordList
  //...

  // create a RecognizerContext for the WordList
  rc = inkEdit1.Recognizer.CreateRecognizerContext();
  rc.Factoid = Factoid.WordList;

  //set the RecognizerContext WordList to the newly created WordList
  rc.WordList = wl;

  //create a delegate for the new RecognizerContext
  rc.RecognitionWithAlternates += new

  RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition);
}

void inkEdit1_TextChanged(object sender, EventArgs e)
{
  if (isRecoPending)
  {
    isRecoPending = false;
    rc.BackgroundRecognizeWithAlternates();
  }
}

private void inkEdit1_Recognition(object sender,
Microsoft.Ink.InkEditRecognitionEventArgs e)
{
  //store the start of the selection in wlSelStart
  wlSelStart = inkEdit1.SelectionStart;

  //store the length of the selection in wlSelLen
  wlSelLen = e.RecognitionResult.TopString.Length;

  //copy the strokes from the InkEdit control into the new
  // RecognizerContext
  rc.Strokes = e.RecognitionResult.Strokes.Ink.Clone().Strokes;
  isRecoPending = true;
}

private void rc_Recognition(object sender,
Microsoft.Ink.RecognizerContextRecognitionWithAlternatesEventArgs e)
{
  if (inkEdit1.InvokeRequired)
  {
    inkEdit1.Invoke(new RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition),
      new object[] { sender, e });
    return;
  }

  //set the insertion point in the InkEdit control
  inkEdit1.SelectionStart = wlSelStart;
  inkEdit1.SelectionLength = wlSelLen;
  //insert the result from the new RecognizerContext 
  //into the InkEdit control
  inkEdit1.SelectedText = e.Result.TopString;
  inkEdit1.SelectionStart = inkEdit1.SelectionStart +
  e.Result.TopString.Length;
}

// Event handler for the form's closed event
private void Form1_Closed(object sender, System.EventArgs e)
{
  inkEdit1.Dispose();
  inkEdit1 = null;
  rc.Dispose();
  rc = null;
}
```



## <a name="related-topics"></a><span data-ttu-id="732b9-109">См. также</span><span class="sxs-lookup"><span data-stu-id="732b9-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="732b9-110">[Элемент управления InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="732b9-110">[InkEdit Control](/previous-versions/ms552265(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="732b9-111">[Класс Microsoft. Ink. Рекогнизерконтекст](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="732b9-111">[Microsoft.Ink.RecognizerContext Class](/previous-versions/ms552546(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="732b9-112">[Класс Microsoft. Ink. список слов](/previous-versions/ms827589(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="732b9-112">[Microsoft.Ink.Wordlist Class](/previous-versions/ms827589(v=msdn.10))</span></span>
</dt> </dl>

 

 
