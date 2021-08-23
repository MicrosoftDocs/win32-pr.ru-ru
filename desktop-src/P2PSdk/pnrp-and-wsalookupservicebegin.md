---
description: Протокол PNRP использует функцию Всалукупсервицебегин для запуска процесса, который позволяет приложению выполнить следующие действия.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP и Всалукупсервицебегин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553404"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP и Всалукупсервицебегин

Протокол PNRP использует функцию [**всалукупсервицебегин**](winsock-nsp-reference-links.md) для запуска процесса, который позволяет приложению выполнять следующие действия:

-   [Разрешение имени](#resolving-a-name)
-   [Перечисление сетевых облаков](#enumerating-network-clouds)

Клиенты, пытающиеся выполнить одну из функций, используют функции [**всалукупсервицебегин**](winsock-nsp-reference-links.md), **всалукупсервиценекст** и **всалукупсервицеенд** .

С помощью [**всанспиоктл**](winsock-nsp-reference-links.md)службу поиска можно использовать асинхронно. Сведения об асинхронном использовании функций службы поиска см. в разделе [PNRP and всанспиоктл](pnrp-and-wsanspioctl.md).

Процесс работы с именами одноранговых узлов отличается от работы с облаками. Каждый процесс описан отдельно в этом разделе.

## <a name="resolving-a-name"></a>Разрешение имени

Приложение использует [**всалукупсервицебегин**](winsock-nsp-reference-links.md) для получения IP-адреса, порта и протокола для одноранговой службы, зарегистрированной на другом компьютере. Функция **всалукупсервицебегин** используется для запуска процесса разрешения имен и настройки параметров и ограничений. Возвращается маркер, который должен использоваться при вызове **всалукупсервиценекст** и **всанспиоктл**.

### <a name="lpqsrestrictions"></a>лпксрестриктионс

При разрешении имени однорангового узла Структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрестриктионс* , должна содержать следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Указывает имя однорангового узла для разрешения.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Должен быть **свЦид \_ пнрпнаме**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**
</dt> <dd>

Должен быть либо **NS \_ пнрпнаме** , либо **NS \_ ALL**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**
</dt> <dd>

Необходимо указать либо **\_ \_ пнрпнаме Provider** , либо **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**
</dt> <dd>

Должно быть именем облака, пустой строкой или **значением NULL**. Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global \_ . В противном случае он должен указывать на допустимое имя облака.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Значение должно быть указателем на структуру [**больших двоичных объектов**](winsock-nsp-reference-links.md) или **null**. Если он имеет **значение NULL**, используются значения по умолчанию. Если задано значение, **лпблоб** указывает на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) , и необходимо задать определенные параметры в структуре **пнрпинфо** . Дополнительные сведения см. в следующих описаниях для структуры ПНРПИНФО.

</dd> </dl>

Структура ПНРПИНФО

Если задан элемент **лпблоб** структуры [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , необходимо установить следующие элементы структуры [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**лпвсзидентити**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**нмаксресолве**
</dt> <dd>

Указывает запрошенное число разрешений.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**двтимеаут**
</dt> <dd>

Указывает запрошенный период ожидания ответов. По умолчанию это 30 секунд. Максимальное значение составляет 600 секунд (10 минут).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**двлифетиме**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**енресолвекритериа**
</dt> <dd>

Должно быть одним из допустимых значений. По умолчанию **используется \_ условие разрешения PNRP, \_ \_ отличное от \_ текущего \_ \_ однорангового узла \_ процесса**. Допустимые значения указываются [**в \_ \_ критериях разрешения PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Должно быть либо нулевым (0), **либо \_ подсказкой пнрпинфо**. Значение по умолчанию равно нулю (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**сахинт**
</dt> <dd>

Указывает IP-адрес для указания. Указание используется при попытке найти ближайшее имя однорангового узла. Подсказка представляет собой IPv6-адрес. Если **сахинт** не указан при поиске ближайшего однорангового имени, вместо него используется IPv6-адрес локального компьютера. Этот элемент игнорируется, если **dwFlags** не задан.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**еннаместате**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>двконтролфлагс

\_ \_ \* PNRP поддерживает следующие флаги возврата Луп:



| Значение                | Описание                                |
|----------------------|--------------------------------------------|
| \_имя возврата \_ Луп    | Возвращает имя и контекст.                |
| \_Комментарий возврата \_ Луп | Возвращает комментарий, связанный с именем.  |
| ЛУП \_ обратный \_ адрес    | Возвращает адрес, связанный с именем. |



 

## <a name="enumerating-network-clouds"></a>Перечисление сетевых облаков

### <a name="lpqsrestrictions"></a>лпксрестриктионс

При перечислении облаков структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрестриктионс* , должна содержать следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Должен иметь **значение NULL**.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Должен быть **свЦид \_ пнрпклауд**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**
</dt> <dd>

Должен быть **\_ пнрпклауд NS**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**
</dt> <dd>

Необходимо указать либо **\_ \_ пнрпклауд Provider** , либо **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Зарезервировано, должно быть **равно NULL**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) . Если **лпблоб** имеет **значение NULL**, перечисляются все облака.

</dd> </dl>

Структура ПНРПКЛАУДИНФО

При перечислении облаков необходимо задать следующие члены структуры [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Вычислений**
</dt> <dd>

Указывает на структуру, задающую критерии, которые можно использовать для фильтрации результатов поиска. **Облако. Scope** может быть **\_ областью PNRP \_ любой**, **\_ глобальной \_ областью PNRP**, **\_ \_ локальной \_ областью сайта PNRP** или **\_ \_ локальной \_ областью связи PNRP**. Если указана **\_ область PNRP \_ ANY** , возвращаются все облака. В противном случае возвращаются только облака, соответствующие **облаку. Scope** .

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**енклаудстате**
</dt> <dd>

Зарезервировано, должно быть равно нулю (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>двконтролфлагс

\_ \_ \* PNRP поддерживает следующие флаги возврата Луп:



| Значение             | Описание                                                       |
|-------------------|-------------------------------------------------------------------|
| \_имя возврата \_ Луп | Возвращает имя и контекст.                                       |
| \_возвращаемый \_ BLOB-объект Луп | Возвращает [большой двоичный объект](pnrp-and-blob.md) , связанный с этим облаком. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[PNRP и BLOB-объект](pnrp-and-blob.md)
</dt> <dt>

[PNRP и Всалукупсервицеенд](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP и Всалукупсервиценекст](pnrp-and-wsalookupservicenext.md)
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
</dt> </dl>

 

 



