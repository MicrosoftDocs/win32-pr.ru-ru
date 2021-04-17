---
title: Метод завершения (устаревшие функции среды Windows)
description: Метод Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701013"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Метод завершения (устаревшие функции среды Windows)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Останавливает анимацию для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_")._ *  \[ *Запрос* на завершение\]



| Отделение      | Описание                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Запрос* | Необязательный элемент. Объект [**запроса**](/windows/desktop/lwef/the-request-object) , указывающий конкретный вызов анимации. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы указать параметр запроса, необходимо создать переменную и назначить запрос анимации, который нужно присвоить. Если параметр **запроса** не задан, сервер останавливает все анимации для символа, включая вызовы [**Get**](get-method.md) , помещенные в очередь, и очищает ее очередь анимации, если этот символ в данный момент не содержит **скрытую** анимацию или не **отображает** ее. Этот метод не останавливает вызовы **Get** , не входящие в очередь.

Чтобы отменить определенную анимацию или вызов [**Get**](get-method.md) , объявите объектную переменную и назначьте запрос анимации этой переменной:


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Этот метод не создаст объект [**запроса**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>См. также:

[**Метод Стопалл**](stopall-method.md)


 

 
