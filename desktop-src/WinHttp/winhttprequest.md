---
Description: В этом разделе содержатся сведения об использовании COM-объекта WinHTTP WinHttpRequest с языками сценариев.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Объект WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 92fdcb9c6eff502dc5f19cb62d92af5d4db60e15890667c894f96cfb55a9e5ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132917"
---
# <a name="winhttprequest-object"></a>Объект WinHttpRequest

В этом разделе содержатся сведения об использовании COM-объекта WinHTTP **WinHttpRequest** с языками сценариев. Дополнительные сведения, включая API C++ (WinHTTP), см. в статье [о WinHTTP](about-winhttp.md). Сравнение этих интерфейсов см. в разделе [Выбор интерфейса WinHTTP](choosing-a-winhttp-interface.md) .

## <a name="example"></a>Пример

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Примеры кода, взятые из [Свойства ивинхттпрекуест:: Status](iwinhttprequest-status.md).



## <a name="members"></a>Элементы

Объект **WinHttpRequest** имеет следующие типы членов:

-   [События](#events)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="events"></a>События

Объект **WinHttpRequest** содержит эти события.



| Событие                                                                            | Описание                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Происходит при возникновении ошибки времени выполнения в приложении.<br/> |
| [**онреспонседатааваилабле**](iwinhttprequestevents-onresponsedataavailable.md) | Происходит при доступе к данным из ответа.<br/>          |
| [**онреспонсефинишед**](iwinhttprequestevents-onresponsefinished.md)           | Происходит при завершении данных ответа.<br/>                |
| [**онреспонсестарт**](iwinhttprequestevents-onresponsestart.md)                 | Происходит при начале получения данных ответа.<br/>      |



 

### <a name="methods"></a>Методы

Объект **WinHttpRequest** содержит эти методы.



| Метод                                                                 | Описание                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Рвал**](iwinhttprequest-abort.md)                                 | Прерывает метод Send [WinHTTP](about-winhttp.md) [](iwinhttprequest-send.md) .<br/>                                                              |
| [**жеталлреспонсехеадерс**](iwinhttprequest-getallresponseheaders.md) | Извлекает все заголовки ответа HTTP.<br/>                                                                                                            |
| [**жетреспонсехеадер**](iwinhttprequest-getresponseheader.md)         | Извлекает заголовки HTTP-ответа.<br/>                                                                                                            |
| [**Открыть**](iwinhttprequest-open.md)                                   | Открывает HTTP-соединение с HTTP-ресурсом.<br/>                                                                                                   |
| [**Отправить**](iwinhttprequest-send.md)                                   | Отправляет HTTP-запрос на сервер HTTP.<br/>                                                                                                        |
| [**сетаутологонполици**](iwinhttprequest-setautologonpolicy.md)       | Задает текущую [политику автоматического входа в систему](authentication-in-winhttp.md).<br/>                                                |
| [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md)   | Выбирает сертификат клиента для отправки на HTTPS-сервер.<br/>                                                    |
| [**сеткредентиалс**](iwinhttprequest-setcredentials.md)               | Задает учетные данные для использования с HTTP-сервером либо исходным, либо прокси-сервером.<br/>                                                             |
| [**сетпрокси**](iwinhttprequest-setproxy.md)                           | Задает сведения о прокси-сервере.<br/>                                                                                                                  |
| [**сетрекуессеадер**](iwinhttprequest-setrequestheader.md)           | Добавляет, изменяет или удаляет заголовок HTTP-запроса.<br/>                                                                                               |
| [**сеттимеаутс**](iwinhttprequest-settimeouts.md)                     | Указывает в миллисекундах отдельные компоненты времени ожидания операции отправки и получения.<br/>                                                     |
| [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md)             | Указывает время ожидания для завершения асинхронного метода [**отправки**](iwinhttprequest-send.md) (в секундах) с необязательным значением времени ожидания.<br/> |



 

### <a name="properties"></a>Свойства

Объект **WinHttpRequest** имеет следующие свойства.



| Свойство                                                            | Тип доступа           | Описание                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Параметр**](iwinhttprequest-option.md)<br/>                 | Чтение/запись<br/> | Задает или получает значение параметра WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Только для чтения<br/>  | Извлекает тело объекта ответа в виде массива байтов без знака.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Только для чтения<br/>  | Извлекает тело объекта ответа в виде [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**респонсетекст**](iwinhttprequest-responsetext.md)<br/>     | Только для чтения<br/>  | Извлекает текст объекта ответа в виде текста.<br/>                          |
| [**Состояние**](iwinhttprequest-status.md)<br/>                 | Только для чтения<br/>  | Извлекает код состояния HTTP из последнего ответа.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Только для чтения<br/>  | Получает текст состояния HTTP.<br/>                                          |



 

## <a name="remarks"></a>Remarks

Объект **WinHttpRequest** использует интерфейс [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) для предоставления данных об ошибках. описание и числовое значение ошибки можно получить с помощью объекта [Err](/previous-versions//sbf5ze0e(v=vs.85)) в microsoft Visual Basic scripting Edition (VBScript) и объекта [ошибки](https://msdn.microsoft.com/library/dww52sbt.aspx) в microsoft JScript. Младшие 16 разрядов номера ошибки соответствуют значениям, находящихся в [**сообщениях об ошибках**](error-messages.md).

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md).

 

## <a name="requirements"></a>Требования



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

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

