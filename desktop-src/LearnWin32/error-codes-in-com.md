---
title: Коды ошибок в COM
description: Коды ошибок в COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103962"
---
# <a name="error-codes-in-com"></a>Коды ошибок в COM

Чтобы указать на успех или неудачу, методы и функции COM возвращают значение типа **HRESULT**. **HRESULT** — это 32-разрядное целое число. Старший бит успешных или неудачных сигналов **HRESULT** . Ноль (0) указывает на успешное выполнение, а 1 — на сбой.

При этом создаются следующие числовые диапазоны:

-   Коды успеха: 0x0 – 0x7FFFFFFF.
-   Коды ошибок: 0x80000000 – 0xFFFFFFFF.

Небольшое количество методов COM не возвращает значение **HRESULT** . Например, методы [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) возвращают неподписанные длинные значения. Но каждый COM-метод, который возвращает код ошибки, делает это, возвращая значение **HRESULT** .

Чтобы проверить, завершился ли метод COM, проверьте старший бит возвращенного **HRESULT**. Заголовки Windows SDK предоставляют два макроса, которые упрощают выполнение следующих действий: макрос « [**успешно**](/windows/desktop/api/winerror/nf-winerror-succeeded) » и [**сбой**](/windows/desktop/api/winerror/nf-winerror-failed) макроса. Макрос  Success возвращает **значение true** , если **HRESULT** является кодом успешного выполнения, и **false** , если это код ошибки. В следующем примере проверяется успешность завершения [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



Иногда удобнее протестировать обратное условие. [**Невыполненный**](/windows/desktop/api/winerror/nf-winerror-failed) макрос выполняет противоположный [**результат.**](/windows/desktop/api/winerror/nf-winerror-succeeded) Он возвращает **значение true** для кода ошибки и **значение false** для кода успешного выполнения.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Далее в этом модуле мы рассмотрим некоторые практические советы по структурированию кода для устранения ошибок COM. (См. раздел [Обработка ошибок в com](error-handling-in-com.md).)

## <a name="next"></a>Следующая

[Создание объекта в COM](creating-an-object-in-com.md)

 

 
