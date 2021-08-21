---
description: Протокол PNRP использует функцию Всалукупсервиценекст для сопоставления запросов, указанных в предыдущем вызове функции Всалукупсервицебегин.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP и Всалукупсервиценекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec10c8021a2f13be1a1ffe228ca73a07c8af10dfc8714bef14f0bddeb0952aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553324"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP и Всалукупсервиценекст

Протокол PNRP использует функцию [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для сопоставления запросов, указанных в предыдущем вызове функции **всалукупсервицебегин**. Результаты функции **всалукупсервиценекст** определяются параметрами в структуре **всакуерисет** , переданной в начальном вызове функции **всалукупсервицебегин** . Эта функция используется для выполнения следующих двух функций:

-   Разрешение имени однорангового узла в список адресов
-   Перечисление сетевых облаков

С помощью [**всанспиоктл**](winsock-nsp-reference-links.md)службу поиска можно использовать асинхронно. Сведения об асинхронном использовании функций службы поиска см. в разделе [PNRP and всанспиоктл](pnrp-and-wsanspioctl.md).

Функция [**всалукупсервиценекст**](winsock-nsp-reference-links.md) блокируется, даже если вызывается **всанспиоктл** . Перед вызовом **всалукупсервиценекст** приложение должно подождать, пока оно не получит уведомление, если блокировка является проблемой.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Разрешение имени однорангового узла в список адресов

При разрешении имени однорангового узла в список адресов структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , возвращаемая в параметре *лпксресултс* , содержит следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Возвращает размер структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Возвращает имя однорангового узла — если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Возвращает **свЦид \_ пнрпнаме**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Возвращает комментарий: Если **Луп \_ возвращает \_ Комментарий**, **Луп \_ возвращает \_ все** или задано **значение NULL** .

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**
</dt> <dd>

Возвращает **\_ пнрпнаме NS**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**
</dt> <dd>

Возвращает **\_ \_ пнрпнаме поставщика NS**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**
</dt> <dd>

Возвращает имя облака, если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Возвращает ноль (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Возвращает количество записей в \_ массиве сведений ксаддр, если **Луп \_ возвращаемый \_ адрес**, **Луп \_ возвращает \_ все** или задано **значение NULL** . Это значение и сведения в **лпксабуффер** являются ключевыми битами информации, возвращаемой этой структурой.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Возвращает указатель на массив \_ структур ксаддр info, если **Луп \_ возвращает \_ АДР**, **Луп \_ возвращает \_ ALL** или **значение NULL** . Этот буфер и значение в **двнумберофксаддрс** являются ключевыми битами данных, возвращаемыми в этой структуре.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Возвращает ноль (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Возвращает **значение NULL**.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Перечисление сетевых облаков

При перечислении облаков структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , возвращаемая в параметре *лпксресултс* , содержит следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Возвращает размер структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Возвращает имя облака — если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Возвращает **свЦид \_ пнрпклауд**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**
</dt> <dd>

Возвращает **\_ пнрпклауд NS**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**
</dt> <dd>

Возвращает **\_ \_ пнрпклауд поставщика NS**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Возвращает ноль (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Возвращает ноль (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Возвращает **значение NULL**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Возвращает ноль (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Возвращает указатель на структуру [**больших двоичных объектов**](winsock-nsp-reference-links.md) , указывающую на структуру [**Пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) : Если **Луп \_ возвращает \_ большой двоичный объект**, **Луп \_ возвратите \_ ALL** или задается **значение NULL** .

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Структура ПНРПКЛАУДИНФО

При перечислении облачных имен в структуре [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) возвращаются следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Вычислений**
</dt> <dd>

Фактическое значение облака.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**енклаудстате**
</dt> <dd>

Текущее состояние облака. Протокол [**PNRP \_ \_Состояние облака**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) указывает допустимые значения.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**енклаудфлагс**
</dt> <dd>

Указывает, что имя облака допустимо в сети или допустимо только на текущем компьютере. Протокол [**PNRP \_ \_Флаги облака**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) указывают допустимые значения. Некоторые облачные имена допустимы на любом компьютере в одной сети. Другие облачные имена действительны только на текущем компьютере и могут быть действительны только в течение определенного периода времени.

-   Если для **енклаудфлагс** задано **значение \_ \_ \_ Локальное облачное имя PNRP,** это имя допустимо только локально.
-   Если **енклаудфлагс** не задан, имя облака можно передать на другие компьютеры.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[PNRP и BLOB-объект](pnrp-and-blob.md)
</dt> <dt>

[PNRP и Всалукупсервицеенд](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP и Всанспиоктл](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP и ВСАКУЕРИСЕТ](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Коды ошибок PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**всалукупсервицебегин**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



