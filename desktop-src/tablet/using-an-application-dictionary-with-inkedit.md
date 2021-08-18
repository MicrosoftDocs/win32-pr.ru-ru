---
description: Чтобы создать словарь приложений, необходимо задать свойство «список слов» объекта Рекогнизерконтекст.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Использование словаря приложения с InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b090b0822afba691012ef19d51068a18c3cf8d6c9afb9070f43f63cd86ef34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966643"
---
# <a name="using-an-application-dictionary-with-inkedit"></a>Использование словаря приложения с InkEdit

Чтобы создать словарь приложений, необходимо задать свойство « [**список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) » объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) . Элемент управления [InkEdit](inkedit-control-reference.md) не предоставляет объект **рекогнизерконтекст** , поэтому невозможно напрямую задать свойство " **список слов** " объекта **рекогнизерконтекст** элемента управления InkEdit.

Чтобы использовать словарь приложения с элементом управления [InkEdit](inkedit-control-reference.md) , необходимо взять штрихи за пределами элемента управления InkEdit, передать их в новый объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) со свойством " [**список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) ", для которого задано значение " [**список слов**](inkwordlist-class.md) ", содержащий словарь приложения, сохранить результаты из этого объекта **рекогнизерконтекст** , а затем передать результаты обратно в элемент управления InkEdit.

## <a name="example"></a>Пример

В следующем коде на языке C \# показан пример этой методики.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элемент управления InkEdit](/previous-versions/ms552265(v=vs.100))
</dt> <dt>

[Класс Microsoft. Ink. Рекогнизерконтекст](/previous-versions/ms552546(v=vs.100))
</dt> <dt>

[Класс Microsoft. Ink. список слов](/previous-versions/ms827589(v=msdn.10))
</dt> </dl>

 

 
