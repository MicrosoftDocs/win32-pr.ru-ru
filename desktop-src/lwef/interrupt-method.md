---
title: Метод прерывания
description: Метод прерывания
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749261"
---
# <a name="interrupt-method"></a>Метод прерывания

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Прерывает анимацию для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Запрос на прерывание_ *  



| Часть      | Описание                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Запрос* | Объект [**запроса**](/windows/desktop/lwef/the-request-object) для конкретного вызова анимации. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Его можно использовать для синхронизации анимации между символами. Например, если другой символ находится в циклической анимации, этот метод останавливает цикл и переходит к следующей анимации в очереди символов. Нельзя прерывать неиспользуемую анимацию символов (которая не была загружена).

Чтобы указать параметр запроса, необходимо создать переменную и назначить запрос анимации, который нужно прервать:


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



Нельзя прерывать анимацию того же символа, который указан в этом методе, так как сервер помещает метод **прерывания** в очередь анимации этого символа. Таким образом, **прерывание** можно использовать только для остановки анимации другого символа, который вы загрузили.

Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .

> [!Note]  
> **Прерывание** не приводит к сбросу очереди символов. Она останавливает существующую анимацию и переходит к следующей анимации в очереди символов. Чтобы остановить и очистить очередь символов, используйте метод [**остановки**](stop-method.md) .

 

## <a name="see-also"></a>См. также

[**Метод Stop**](stop-method.md)


 

 