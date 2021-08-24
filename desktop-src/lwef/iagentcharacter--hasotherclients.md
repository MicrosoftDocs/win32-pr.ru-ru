---
title: Иажентчарактер Хасосерклиентс
description: Иажентчарактер Хасосерклиентс
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6469c289d846cb34e14c6afabbed72647e6e786fbda273baaf70532d4ad6578c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665754"
---
# <a name="iagentcharacterhasotherclients"></a>Иажентчарактер:: Хасосерклиентс

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




