---
title: Иажентчарактер Play
description: Иажентчарактер Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068662"
---
# <a name="iagentcharacterplay"></a>Иажентчарактер::Pный макет

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Воспроизводит указанную анимацию.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно. Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*бсзаниматион*
</dt> <dd>

Имя анимации.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*
</dt> <dd>

Адрес переменной, которая получает идентификатор запроса **иажентчарактер::P** .

</dd> </dl>

Имя анимации определяется при компиляции символа с помощью редактора символов Microsoft Agent. Прежде чем воспроизводить указанную анимацию, сервер пытается воспроизвести анимацию **возврата** для предыдущей анимации (если она была назначена).

Если данные анимации персонажа хранятся на локальном компьютере пользователя, можно использовать метод **иажентчарактер::P макетирования** и указать имя анимации. При использовании протокола HTTP для доступа к данным анимации используйте метод [**Prepare**](iagentcharacter--prepare.md) , чтобы обеспечить доступность анимации перед вызовом этого метода.

## <a name="see-also"></a>См. также:

[**Иажентчарактер::P готовка**](iagentcharacter--prepare.md)


 

 




