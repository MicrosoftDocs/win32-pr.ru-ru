---
title: Иажентчарактер Play
description: Иажентчарактер Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976404"
---
# <a name="iagentcharacterplay"></a>Иажентчарактер::Pный макет

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




