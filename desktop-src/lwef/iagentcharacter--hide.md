---
title: Иажентчарактер скрыть
description: Иажентчарактер скрыть
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069927"
---
# <a name="iagentcharacterhide"></a>Иажентчарактер:: Hide

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Скрывает символ.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно. Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*бфаст*
</dt> <dd>

**Скрытие** флага анимации состояния. Если этот параметр имеет **значение true**, то **Скрытая** анимация не воспроизводится до скрытия рамки символов. Если задано **значение false**, анимация будет воспроизводиться.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*
</dt> <dd>

Адрес переменной, которая получает идентификатор запроса **скрытия** .

</dd> </dl>

Сервер помещает в очередь анимацию, связанную с методом **Hide** в очереди символов. Это позволяет использовать его для скрытия символа после последовательности других анимаций. Вы можете воспроизвести действие немедленно с помощью метода « [**останавливаться**](iagentcharacter--stop.md) » перед вызовом метода **Hide** .

При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность анимации **скрытого** состояния перед вызовом этого метода.

Скрытие символа может также вызвать событие [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md) другого видимого символа.

Скрытые символы не могут получить доступ к каналу аудио. Сервер передаст состояние сбоя в событии [**рекуесткомплете**](iagentnotifysink--requestcomplete.md) , если создается запрос анимации и этот символ скрыт.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: показывать**](iagentcharacter--show.md)


 

 