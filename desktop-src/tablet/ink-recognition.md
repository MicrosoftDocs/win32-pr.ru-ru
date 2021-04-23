---
description: Не все приложения используют распознавание, но так как большинство приложений разрабатывались с использованием текста в качестве первичного типа данных, возможность преобразования рукописного ввода в текст очень важна.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Распознавание рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562389"
---
# <a name="ink-recognition"></a><span data-ttu-id="bfc86-103">Распознавание рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="bfc86-103">Ink Recognition</span></span>

<span data-ttu-id="bfc86-104">Не все приложения используют распознавание, но так как большинство приложений разрабатывались с использованием текста в качестве первичного типа данных, возможность преобразования рукописного ввода в текст очень важна.</span><span class="sxs-lookup"><span data-stu-id="bfc86-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="bfc86-105">Функции распознавания API платформы Tablet PC можно использовать для запроса информации о доступных механизмах распознавания, например о том, какие языки они распознают.</span><span class="sxs-lookup"><span data-stu-id="bfc86-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="bfc86-106">Затем можно отправить коллекцию [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) из объекта [**рукописного ввода**](inkdisp-class.md) в механизм распознавания и вернуть объект [**рекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="bfc86-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="bfc86-107">Объект Рекогнизерконтекст</span><span class="sxs-lookup"><span data-stu-id="bfc86-107">RecognizerContext Object</span></span>

<span data-ttu-id="bfc86-108">Объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) — это экземпляр данного распознавателя.</span><span class="sxs-lookup"><span data-stu-id="bfc86-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="bfc86-109">Объект **рекогнизерконтекст** позволяет распознать заданную коллекцию штрихов синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bfc86-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="bfc86-110">При асинхронном распознавании объект **рекогнизерконтекст** возвращает объект [**рекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) в обратном вызове события в приложение.</span><span class="sxs-lookup"><span data-stu-id="bfc86-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="bfc86-111">Распознаватели и объекты распознавателя</span><span class="sxs-lookup"><span data-stu-id="bfc86-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="bfc86-112">У одного планшетного компьютера может быть один или несколько распознаваемых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bfc86-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="bfc86-113">Вы можете запросить коллекцию распознавателя, чтобы определить, какой распознаватель использовать.</span><span class="sxs-lookup"><span data-stu-id="bfc86-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="bfc86-114">Распознаватель предоставляет определенные сведения о своих возможностях, такие как язык, который он может распознать, и производитель.</span><span class="sxs-lookup"><span data-stu-id="bfc86-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="bfc86-115">Чтобы определить, установлен ли хотя бы один распознаватель, создайте экземпляр объекта [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) , как показано в следующих \# примерах кода C++ и C.</span><span class="sxs-lookup"><span data-stu-id="bfc86-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="bfc86-116">Если распознаватель отсутствует, вызов [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="bfc86-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="bfc86-117">Объекты Рекогнитионресулт и Рекогнитионалтернате</span><span class="sxs-lookup"><span data-stu-id="bfc86-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="bfc86-118">Результаты распознавания возвращаются в объекте [**рекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="bfc86-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="bfc86-119">Результаты содержат лучшую результирующую строку в свойстве [топстринг](/previous-versions/ms829602(v=msdn.10)) , а также коллекцию альтернативных результатов в коллекции [**рекогнитионалтернатес**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) .</span><span class="sxs-lookup"><span data-stu-id="bfc86-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="bfc86-120">Объект **рекогнитионресулт** может быть сохранен в исходной коллекции [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , из которой он был создан.</span><span class="sxs-lookup"><span data-stu-id="bfc86-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="bfc86-121">Структура Рекогнизергуиде</span><span class="sxs-lookup"><span data-stu-id="bfc86-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="bfc86-122">Руководству по распознавателю может состоять из строк и столбцов, а также предоставляет распознавателю Улучшенный контекст, в котором выполняется распознавание.</span><span class="sxs-lookup"><span data-stu-id="bfc86-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="bfc86-123">Например, можно нарисовать горизонтальные линии на экране пользователя, почти так же, как часть бумаги с линейкой, которая показывает, где должно происходить рукописное письмо (этот тип руководств будет состоять только из строк и не содержит столбцов).</span><span class="sxs-lookup"><span data-stu-id="bfc86-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="bfc86-124">Если пользователь записывает строки, а не какой-либо произвольный пробел, то точность распознавания повысится.</span><span class="sxs-lookup"><span data-stu-id="bfc86-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="bfc86-125">На следующем рисунке показана структура [**рекогнизергуиде**](inkrecognizerguide-class.md) с двумя строками для входных данных.</span><span class="sxs-lookup"><span data-stu-id="bfc86-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![Иллюстрация с руководством по двум строкам](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="bfc86-127">На следующем рисунке показана структура [**рекогнизергуиде**](inkrecognizerguide-class.md) с четырьмя столбцами и тремя строками.</span><span class="sxs-lookup"><span data-stu-id="bfc86-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![Иллюстрация с руководством "три на четыре"](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="bfc86-129">Дополнительные сведения об использовании структуры [**рекогнизергуиде**](inkrecognizerguide-class.md) см. в разделе Справочник по **рекогнизергуиде** .</span><span class="sxs-lookup"><span data-stu-id="bfc86-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
