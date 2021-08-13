---
description: Выбирает сертификат клиента для отправки на HTTPS-сервер.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Метод Ивинхттпрекуест:: Сетклиентцертификате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562900"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Метод Ивинхттпрекуест:: Сетклиентцертификате

Метод **сетклиентцертификате** выбирает сертификат клиента для отправки на HTTPS-сервер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Clientcertificate* \[ окне\]
</dt> <dd>

Указывает расположение, [*хранилище сертификатов*](glossary.md)и субъект сертификата клиента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Remarks

Строка, указанная в параметре *clientcertificate* , состоит из расположения сертификата, хранилища сертификатов и имени субъекта, разделенных символами обратной косой черты. Дополнительные сведения о компонентах строки сертификата см. в разделе [Client Certificates](ssl-in-winhttp.md).

Имя и расположение хранилища сертификатов являются необязательными. Однако если указать хранилище сертификатов, необходимо также указать расположение этого хранилища сертификатов. Расположение по умолчанию — текущий \_ пользователь, а хранилище сертификатов по умолчанию — "My". Пустой субъект указывает, что следует использовать первый сертификат в хранилище сертификатов.

Вызовите **сетклиентцертификате** , чтобы выбрать сертификат перед вызовом [**Send**](iwinhttprequest-send.md) для отправки запроса.

службы Microsoft Windows HTTP (WinHTTP) не предоставляют сертификаты клиента прокси-серверам, запрашивающим сертификаты для проверки подлинности.

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="examples"></a>Примеры

В следующем примере скрипта показано, как выбрать сертификат клиента для отправки с запросом. Сертификат с темой "мой Middle-Tier сертификат" выбирается из хранилища сертификатов "Личное" в реестре в разделе **hKey \_ локальный \_ компьютер**. поскольку этот пример кода характерен для JScript Microsoft, который использует обратную косую черту в качестве escape-символа, для разделения компонентов строки сертификата должны использоваться две смежные обратные косые черты.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивинхттпрекуест**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SSL в WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




