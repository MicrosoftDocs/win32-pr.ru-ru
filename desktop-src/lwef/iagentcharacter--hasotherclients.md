---
title: Иажентчарактер Хасосерклиентс
description: Иажентчарактер Хасосерклиентс
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532501"
---
# <a name="iagentcharacterhasotherclients"></a>Иажентчарактер:: Хасосерклиентс

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

Возвращает значение, указывающее, есть ли у символа другие клиенты.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*плнумосерклиентс*
</dt> <dd>

Адрес переменной, которая получает число других подключенных клиентов для символа (общее число клиентов за вычетом клиента).

</dd> </dl>

 

 




