---
description: Для регистрации или удаления одноранговых имен в PNRP используется функция Всасетсервице.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP и Всасетсервице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afbc11e65c9d583f91b5070e960435612ad05717b6ccfe087924da133c531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518104"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP и Всасетсервице

Для регистрации или удаления [одноранговых имен](peer-names.md)в PNRP используется функция [**всасетсервице**](winsock-nsp-reference-links.md) .

## <a name="registering-a-name"></a>Регистрация имени

Регистрация включает имя однорангового узла и набор конечных точек, с которыми можно связаться со службой. Регистрация зависит от облака PNRP. После регистрации однорангового узла между регистрацией и распространением сведений о регистрации на другие узлы возникает задержка. В течение этого времени другие узлы, возможно, не смогут разрешить только что зарегистрированный одноранговый узел.

Регистрация службы не является постоянной.

-   Если клиентский процесс, регистрирующий имя однорангового узла, завершает работу или вызывает [**всаклеануп**](winsock-nsp-reference-links.md), то имя однорангового узла отменяется.
-   Если указанное имя однорангового узла уже зарегистрировано в том же облаке текущим процессом, оно заменяется новыми значениями регистрации.

При регистрации имени однорангового узла должны быть указаны следующие значения параметров:

-   параметр *ессоператион* должен иметь значение **рнрсервице \_ Register**.
-   параметр *двконтролфлагс* должен быть равен нулю (0).

При регистрации имени однорангового узла Структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрегинфо* , должна содержать следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Указывает имя однорангового узла для регистрации. Если [имя однорангового узла](peer-names.md) не защищено, то удостоверение является необязательным. Если удостоверение указано как **null**, по умолчанию PNRP использует локальное удостоверение компьютера.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Должен быть СВЦИД \_ пнрпнаме.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Не обрабатывается. Однако строка по-прежнему должна содержать менее 40 символов, включая знак завершения **null** .

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

Должно быть именем облака, пустой строкой или **значением NULL**. Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global. В противном случае он должен указывать на допустимое имя облака.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Указывает количество адресов, зарегистрированных службой. Максимальное число адресов, которое можно зарегистрировать для одного имени, равно 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Указатель на список адресов для регистрации.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Необходимо задать определенные параметры в структуре **пнрпинфо** . Дополнительные сведения см. в следующем разделе структуры **пнрпинфо** .

</dd> </dl>

## <a name="pnrpinfo-structure"></a>Структура ПНРПИНФО

Если задан элемент **лпблоб** структуры [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , необходимо установить следующие элементы структуры [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**лпвсзидентити**
</dt> <dd>

Указывает идентификатор имени однорангового узла, созданного с помощью [**пиридентитикреате**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Если имя однорангового узла не защищено, то удостоверение является необязательным. Если удостоверение указано как **null**, по умолчанию PNRP использует локальное удостоверение компьютера.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**нмаксресолве**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**двтимеаут**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**двлифетиме**
</dt> <dd>

Указывает количество секунд между операциями обновления.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**енресолвекритериа**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Должно быть либо нулевым (0), **либо \_ подсказкой пнрпинфо**. Значение по умолчанию равно нулю (0). Это означает, что часть расположения службы в ИДЕНТИФИКАТОРе PNRP строится с помощью IP-адреса в **сахинт**. В противном случае расположение службы строится с помощью первого IP-адреса в первой записи IPv6 члена **лпксабуффер** .

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**сахинт**
</dt> <dd>

Указывает IPv6-адрес для указания.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**еннаместате**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Отмена регистрации имени однорангового узла

В следующем списке приведены важные сведения об отмене регистрации имени однорангового узла.

-   Только приложение, которое регистрирует одноранговое имя, может отменить его регистрацию.
-   Отмена регистрации имени однорангового узла выполняется автоматически при вызове [**всаклеануп**](winsock-nsp-reference-links.md) .
-   Протокол PNRP всегда удаляет всю регистрацию имени службы. Удаление отдельных адресов не допускается.
-   При отмене регистрации имени параметр *ессоператион* должен иметь значение **рнрсервице \_ Delete**.
-   PNRP не поддерживает значение **рнрсервице \_ Unregister**.
-   Параметр *двконтролфлагс* должен быть равен нулю (0).

При отмене регистрации имени структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрегинфо* , должна содержать следующие значения:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Задает размер этой структуры.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**
</dt> <dd>

Указывает имя однорангового узла для отмены регистрации.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**
</dt> <dd>

Должен быть **свЦид \_ пнрпнаме**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

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

Должно быть именем облака, пустой строкой или **значением NULL**. Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global. В противном случае он должен указывать на допустимое имя облака.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**
</dt> <dd>

Не обрабатывается. Задайте **значение NULL**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**
</dt> <dd>

Не обрабатывается. Установите нулевое значение (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**
</dt> <dd>

Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Элемент **лпсзидентити** структуры **лпблоб** определяет имя удостоверения, которое используется для регистрации имени однорангового узла. Остальные элементы должны иметь те же значения, которые используются при регистрации имени.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[PNRP и BLOB-объект](pnrp-and-blob.md)
</dt> <dt>

[PNRP и ВСАКУЕРИСЕТ](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Коды ошибок PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**всаклеануп**](winsock-nsp-reference-links.md)
</dt> <dt>

**всасетсервице**
</dt> </dl>

 

 



