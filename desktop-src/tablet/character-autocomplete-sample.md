---
description: В примере с автозаполнением показано, как реализовать Автозаполнение символов на японском языке с помощью интерфейсов прикладного программирования (API) распознавания.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Пример автозаполнения символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539452"
---
# <a name="character-autocomplete-sample"></a>Пример автозаполнения символов

В примере с автозаполнением показано, как реализовать Автозаполнение символов на японском языке с помощью интерфейсов прикладного программирования (API) распознавания.

В этом примере используются следующие функции.

-   Использование *сборщика рукописных данных*
-   Использование *контекста распознавателя*

## <a name="initializing-the-ink-collector-and-recognizer-context"></a>Инициализация сборщика рукописных данных и контекста распознавателя

Объекты [**InkCollector**](inkcollector-class.md) и [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) объявляются как классы, которые могут создавать события.


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



Обработчик событий загрузки формы создает сборщик рукописных данных, связывает его со списком рукописных данных и включает сбор рукописных данных. Затем обработчик событий загружает распознаватель японского языка по умолчанию и инициализирует свойства "Путеводитель" и "Штрихs" для контекста распознавателя.


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a>Загрузка распознавателя японского языка по умолчанию

Метод [**жетдефаултрекогнизер**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) класса [**инкрекогнизерс**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) вызывается для получения распознавателя по умолчанию для японского языка. Далее проверяется свойство [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) объекта иинкрекогнизер, чтобы определить, поддерживает ли распознаватель японский язык. Если это так, то для создания контекста распознавателя для формы используется метод [**креатерекогнизерконтекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) распознавателя.


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a>Обработка события Stroke

Обработчик событий [**Stroke**](inkcollector-stroke.md) сначала останавливает распознавание фона в контексте распознавателя. Затем он добавляет новый росчерк в свойство [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) контекста распознавателя. Наконец, задается свойство [**инкрекогнизерчарактераутокомплетионмоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) контекста распознавателя и вызывается метод [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) контекста распознавателя для каждого из трех режимов автозаполнения символов. Параметр *CustomData* вызова метода **баккграундрекогнизевисалтернатес** используется для указания результатов распознавания, возвращаемых в событии [**рекогнитионвисалтернатес**](inkrecognizercontext-recognitionwithalternates.md) .


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a>Обработка события «распознавание с помощью альтернатив»

Обработчик события [**рекогнитионвисалтернатес**](inkrecognizercontext-recognitionwithalternates.md) сначала проверяет параметр *рекогнитионстатус* . Если при распознавании возникает ошибка, обработчик событий игнорирует результаты распознавания. В противном случае обработчик событий добавляет параметр *рекогнитионресулт* к соответствующему полю изображения и сохраняет результирующую строку. Параметр *CustomData* задается в вызове метода [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) и определяет, какой режим автозаполнения символов использовался в контексте распознавателя.


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a>Рисование формы

Обработчик событий Paint очищает графические поля результатов и добавляет к ним сохраненные результаты распознавания.

## <a name="deleting-the-strokes"></a>Удаление штрихов

`CmdClear_Click`Метод формы обрабатывает команду Clear. Если объект [**InkCollector**](inkcollector-class.md) в настоящее время собирает рукописный ввод, отображается окно сообщения, а команда игнорируется. В противном случае обработчик событий останавливает распознавание фона, очищает свойство [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) контекста распознавателя и удаляет штрихи из объекта [**инкдисп**](inkdisp-class.md) формы. Затем обработчик событий перерисовывает поле рисунка, с которым связан сборщик рукописных данных, и очищает строки распознавания и поля изображений.


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
