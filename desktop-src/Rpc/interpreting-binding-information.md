---
title: Анализ сведений о привязке
description: Microsoft RPC позволяет клиентским и серверным программам получать доступ к информации и интерпретировать ее в маркере привязки.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Удаленный вызов процедур RPC, задачи, интерпретируемая привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487029"
---
# <a name="interpreting-binding-information"></a>Анализ сведений о привязке

Microsoft RPC позволяет клиентским и серверным программам получать доступ к информации и интерпретировать ее в маркере привязки. Это не означает, что вы можете или попытаться напрямую обратиться к содержимому обработчика привязки. Microsoft RPC предоставляет функции, которые задают и извлекают сведения в дескрипторах привязки.

Чтобы получить сведения в маркере привязки, передайте этот обработчик в [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Он возвращает сведения о привязке в виде строки. Для каждого вызова **рпкбиндингтострингбиндинг** необходимо иметь соответствующий вызов функции [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

Можно вызвать функцию [**рпкстрингбиндингпарсе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) для анализа строки, полученной из [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Эта функция выделяет строки, содержащие анализируемые данные. Если не нужно анализировать определенный фрагмент сведений о привязке, передайте значение **null** в качестве значения этого параметра. Обязательно вызывайте [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) для каждой из строк, которые он выделяет.

В следующем фрагменте кода показано, как приложение может вызывать эти функции.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



Предыдущий пример кода вызывает функции [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) и [**рпкстрингбиндингпарсе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) для получения и анализа информации в допустимом маркере привязки. Обратите внимание, что значение **null** было передано в качестве второго параметра для **рпкстрингбиндингпарсе**. Это приводит к тому, что функция пропускает синтаксический анализ идентификатора UUID объекта. Так как он не анализирует UUID, **рпкстрингбиндингпарсе** не будет выделять для него строку. Эта методика позволяет приложению выделить только память для сведений, которые необходимы для анализа и анализа.

 

 




