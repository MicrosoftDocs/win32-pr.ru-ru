---
description: Отправка запросов состояния Копп
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Отправка запросов состояния Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805212"
---
# <a name="sending-copp-status-requests"></a>Отправка запросов состояния Копп

Чтобы отправить запрос о состоянии сертифицированного протокола выходной защиты (Копп), заполните структуру [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) данными запроса. Члены структуры:

-   **Рапп**. 128-разрядное случайное число, введенное как идентификатор GUID. В ответе драйвера возвращается то же число. Необходимо выделить случайное число в куче, а затем скопировать его в структуру. Это защищает от атак, в которых злоумышленник изменяет содержимое структуры [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .
-   **гуидстатусрекуестид**. Идентификатор GUID, определяющий запрос. См. [Справочник по запросам Копп](copp-query-reference.md).
-   **двсекуенце**. Порядковый номер состояния. Увеличить это значение после каждого запроса состояния. (В разделе, [запускающем сеанс Копп](initiating-a-copp-session.md), это значение отображается как *устатуссек* в примерах кода.)
-   **кбсизедата**. Размер (в байтах) дополнительных данных, необходимых для запроса.
-   **StatusData**. Данные для запроса состояния.

Передайте структуру [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) в метод [**Иамцертифиедаутпутпротектион::P ротектионстатус**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) . Например, следующий код отправляет запрос состояния, который запрашивает доступные механизмы защиты:


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



Ответ записывается в элемент **коппстатус** структуры [**амкоппстатусаутпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) . Размер допустимых данных в ответе указывается в элементе **кбсизедата** . Чтобы обеспечить целостность сообщения, драйвер рассчитывает код проверки подлинности сообщения (MAC) с помощью алгоритма ОМАК 1 и возвращает это значение в элемент **маккди** структуры. Приложение должно проверить это значение следующим образом:

1.  Вычислите тег ОМАК для блока данных, который отображается после элемента **маккди** структуры [**амкоппстатусаутпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (иными словами, **кбсизедата** и **коппстатус**).
2.  Сравните этот тег со значением в **маккди**, используя прямую **memcmp**.

Алгоритм ОМАК 1 подробно описан в разделе [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . Копп использует следующие параметры ОМАК-1:

-   E = AES
-   t = 128 бит

Данные, возвращаемые запросом состояния, всегда начинаются с двух элементов:

-   То же значение **Рапп** , которое было передано приложением. Следует убедиться, что это значение совпадает с исходным значением, хранящимся в куче.
-   Значение [**Копп \_ статусфлагс**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) , указывающее, изменилось ли состояние защиты вывода.

Так как подключение может быть потеряно или перенастроено, приложение должно периодически опрашивать драйвер на предмет текущего состояния. Если установлен \_ флаг Копп ренеготиатионрекуиред, приложение должно попытаться сбросить уровень защиты. Если установлен \_ флаг Копп линклост, приложение должно закончить воспроизведение содержимого. Например, \_ можно вернуть флаг Копп линклост, так как пользователь отключил выходной соединитель. Приложение должно освободить текущий экземпляр VMR, создать новый экземпляр VMR и установить новый сеанс Копп (включая обмен ключами и проверку сертификата).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование протокола сертифицированной выходной защиты (Копп)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



