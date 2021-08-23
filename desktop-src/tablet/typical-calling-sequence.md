---
description: 'Методы, которые необходимо реализовать для создания распознавателя рукописного ввода, вызываются API платформы планшетных ПК, а не напрямую с помощью приложения с поддержкой рукописного ввода. Следующие шаги представляют типичную последовательность вызова для реализации этих методов: загружена библиотека DLL.&\# 160; Создан обработчик ХРЕКОГНИЗЕР.&\# 160; Создан обработчик ХРЕКОКОНТЕКСТ. Параметры и режимы распознавателя задаются для этого контекста. Штрихи добавляются к данным рукописного ввода. Входные данные завершены. Рукописный ввод распознан. Результаты распознавания будут возвращены. Обработчик ХРЕКОКОНТЕКСТ уничтожается. Обработчик ХРЕКОГНИЗЕР уничтожается. Вызывающая последовательность также показана в следующем коде: C + + Креатерекогнизер (CLSID, &хрек); Хотя (больше фрагментов рукописного ввода для распознавания...) {//Создание контекста по одному элементу рукописного ввода для распознавания ХРК = CreateContext (хрек, &ХРК);//функции для настройки параметров и режимов для этого контекста Сетгуиде (ХРК, Пгуиде, 0); Сетфактоид (ХРК, 5, PHONE); только если в приложении с Forms Сетфлагс (ХРК, РЕКОФЛАГ \_ вордмоде);//редкими словами, только в том случае, если выбран режим слова, без словаря или один сегмент сетвордлист (ХРК, хвл);//Добавление всех штрихов в этом фрагменте рукописного ввода (больше штрихов...) {Аддстроке (ХРК, NULL, 800, Ппаккет, Пксформ);//один вызов для каждой черты Ендинкинпут (ХРК); Это получает процесс распознавания рукописного ввода (ХРК); Если это простое приложение, оно вызывает его для простого ответа Жетбестресултстринг (ХРК, Length, buffer). Если это сложное приложение, оно вызывает его для получения полного ответа Жетлаттицептр (ХРК, &Платтице); Уничтожить контекст Дестройконтекст (ХРК); }//Вызывается непосредственно перед завершением работы приложения Дестройрекогнизер (хрек);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Типичная последовательность вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94506d320d2ac0dca31fcc44714d0fd9ed089a2dda479020d860b0fbe5bfae5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708224"
---
# <a name="typical-calling-sequence"></a>Типичная последовательность вызовов

Методы, которые необходимо реализовать для создания распознавателя рукописного ввода, вызываются API платформы планшетных ПК, а не напрямую с помощью приложения с поддержкой рукописного ввода.

Следующие шаги представляют типичную последовательность вызова для реализации этих методов:

1.  Библиотека DLL загружена.
2.  Создается обработчик [хрекогнизер](hrecognizer-handle.md) .
3.  Создается обработчик [хрекоконтекст](hrecocontext-handle.md) .
4.  Параметры и режимы распознавателя задаются для этого контекста.
5.  Штрихи добавляются к данным рукописного ввода.
6.  Входные данные завершены.
7.  Рукописный ввод распознан.
8.  Результаты распознавания будут возвращены.
9.  Обработчик [хрекоконтекст](hrecocontext-handle.md) уничтожается.
10. Обработчик [хрекогнизер](hrecognizer-handle.md) уничтожается.

Вызывающая последовательность также показана в следующем коде:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[API-интерфейсы распознавателя](recognizer-apis.md)
</dt> <dt>

[Архитектура API распознавания](recognition-api-architecture.md)
</dt> </dl>

 

 



