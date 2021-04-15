---
description: 'Методы, которые необходимо реализовать для создания распознавателя рукописного ввода, вызываются API платформы планшетных ПК, а не напрямую с помощью приложения с поддержкой рукописного ввода. Следующие шаги представляют типичную последовательность вызова для реализации этих методов: загружена библиотека DLL.&\# 160; Создан обработчик ХРЕКОГНИЗЕР.&\# 160; Создан обработчик ХРЕКОКОНТЕКСТ. Параметры и режимы распознавателя задаются для этого контекста. Штрихи добавляются к данным рукописного ввода. Входные данные завершены. Рукописный ввод распознан. Результаты распознавания будут возвращены. Обработчик ХРЕКОКОНТЕКСТ уничтожается. Обработчик ХРЕКОГНИЗЕР уничтожается. Вызывающая последовательность также показана в следующем коде: C + + Креатерекогнизер (CLSID, &хрек); Хотя (больше фрагментов рукописного ввода для распознавания...) {//Создание контекста по одному элементу рукописного ввода для распознавания ХРК = CreateContext (хрек, &ХРК);//функции для настройки параметров и режимов для этого контекста Сетгуиде (ХРК, Пгуиде, 0); Сетфактоид (ХРК, 5, PHONE); только если в приложении с Forms Сетфлагс (ХРК, РЕКОФЛАГ \_ вордмоде);//редкими словами, только в том случае, если выбран режим слова, без словаря или один сегмент сетвордлист (ХРК, хвл);//Добавление всех штрихов в этом фрагменте рукописного ввода (больше штрихов...) {Аддстроке (ХРК, NULL, 800, Ппаккет, Пксформ);//один вызов для каждой черты Ендинкинпут (ХРК); Это получает процесс распознавания рукописного ввода (ХРК); Если это простое приложение, оно вызывает его для простого ответа Жетбестресултстринг (ХРК, Length, buffer). Если это сложное приложение, оно вызывает его для получения полного ответа Жетлаттицептр (ХРК, &Платтице); Уничтожить контекст Дестройконтекст (ХРК); }//Вызывается непосредственно перед завершением работы приложения Дестройрекогнизер (хрек);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Типичная последовательность вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702474"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="ce029-103">Типичная последовательность вызовов</span><span class="sxs-lookup"><span data-stu-id="ce029-103">Typical Calling Sequence</span></span>

<span data-ttu-id="ce029-104">Методы, которые необходимо реализовать для создания распознавателя рукописного ввода, вызываются API платформы планшетных ПК, а не напрямую с помощью приложения с поддержкой рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ce029-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="ce029-105">Следующие шаги представляют типичную последовательность вызова для реализации этих методов:</span><span class="sxs-lookup"><span data-stu-id="ce029-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="ce029-106">Библиотека DLL загружена.</span><span class="sxs-lookup"><span data-stu-id="ce029-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="ce029-107">Создается обработчик [хрекогнизер](hrecognizer-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="ce029-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="ce029-108">Создается обработчик [хрекоконтекст](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="ce029-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="ce029-109">Параметры и режимы распознавателя задаются для этого контекста.</span><span class="sxs-lookup"><span data-stu-id="ce029-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="ce029-110">Штрихи добавляются к данным рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ce029-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="ce029-111">Входные данные завершены.</span><span class="sxs-lookup"><span data-stu-id="ce029-111">Input is ended.</span></span>
7.  <span data-ttu-id="ce029-112">Рукописный ввод распознан.</span><span class="sxs-lookup"><span data-stu-id="ce029-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="ce029-113">Результаты распознавания будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="ce029-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="ce029-114">Обработчик [хрекоконтекст](hrecocontext-handle.md) уничтожается.</span><span class="sxs-lookup"><span data-stu-id="ce029-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="ce029-115">Обработчик [хрекогнизер](hrecognizer-handle.md) уничтожается.</span><span class="sxs-lookup"><span data-stu-id="ce029-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="ce029-116">Вызывающая последовательность также показана в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="ce029-116">The calling sequence is also illustrated in the following code outline:</span></span>


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a><span data-ttu-id="ce029-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ce029-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce029-118">API-интерфейсы распознавателя</span><span class="sxs-lookup"><span data-stu-id="ce029-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="ce029-119">Архитектура API распознавания</span><span class="sxs-lookup"><span data-stu-id="ce029-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



