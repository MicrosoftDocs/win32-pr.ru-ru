---
title: Иажентусеринпут Жеталлитемдата
description: Иажентусеринпут Жеталлитемдата
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486533"
---
# <a name="iagentuserinputgetallitemdata"></a>Иажентусеринпут:: Жеталлитемдата

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Извлекает данные для всех вариантов [**команд**](command-event.md) , передаваемых в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*пдвитеминдицес*
</dt> <dd>

Адрес переменной, которая получает идентификаторы [**команд**](command-event.md) , переданных в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*плконфиденцес*
</dt> <dd>

Адрес переменной, получающей показатели достоверности для вариантов [**команд**](command-event.md) , передаваемых в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*пбсзтекст*
</dt> <dd>

Адрес переменной, которая получает текст голоса для вариантов [**команд**](command-event.md) , передаваемых обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Если речевое вход активирует [**иажентнотифисинк:: Command**](iagentnotifysink--command.md), сервер возвращает лучшее соответствие, второе — лучшее и третье соответствие, если они предоставляются модулем распознавания речи. Он обеспечивает относительный показатель достоверности в диапазоне от-100 до 100, а фактический текст "слышал" подсистемой распознавания речи. Если наиболее подходящее совпадение было команда, предоставляемая сервером, сервер отправляет идентификатор NULL, но по-прежнему отправляет оценку достоверности и текст [**голоса**](voice-property.md) .

Значение, если речевой ввод не является источником события; Например, если пользователь выбрал команду из всплывающего меню символа, сервер Microsoft Agent возвращает идентификатор выбранной [**команды**](command-event.md) с показателем достоверности 100 и голосовым текстом, равным null. Другие варианты возвращают значение NULL с показателями достоверности ноль (0) и Voice Text как NULL.

> [!Note]  
> Не все модули распознавания речи могут возвращать все значения для всех параметров этого события. Обратитесь к поставщику подсистемы, чтобы определить, поддерживает ли подсистема интерфейс API распознавания речи Майкрософт для возврата альтернатив и оценки достоверности.

 

## <a name="see-also"></a>См. также:

[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md), [**иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md)


 

 




