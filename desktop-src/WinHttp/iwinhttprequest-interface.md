---
description: интерфейс ивинхттпрекуест предоставляет все нечетные методы для служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Интерфейс Ивинхттпрекуест
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 87a31ebe116726d70eb847fe54d563be57477f7133147226657c4c74135defa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114403"
---
# <a name="iwinhttprequest-interface"></a>Интерфейс Ивинхттпрекуест

интерфейс **ивинхттпрекуест** предоставляет все нечетные методы для [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md).

## <a name="members"></a>Элементы

Интерфейс **ивинхттпрекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ивинхттпрекуест** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **ивинхттпрекуест** содержит следующие методы.



| Метод                                                                 | Описание                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Рвал**](iwinhttprequest-abort.md)                                 | Прерывает метод Send [WinHTTP](about-winhttp.md) [](iwinhttprequest-send.md) .<br/>                                           |
| [**жеталлреспонсехеадерс**](iwinhttprequest-getallresponseheaders.md) | Извлекает все заголовки ответа HTTP.<br/>                                                                                         |
| [**жетреспонсехеадер**](iwinhttprequest-getresponseheader.md)         | Извлекает заголовки HTTP-ответа.<br/>                                                                                         |
| [**Открыть**](iwinhttprequest-open.md)                                   | Открывает HTTP-соединение с HTTP-ресурсом.<br/>                                                                                |
| [**Отправить**](iwinhttprequest-send.md)                                   | Отправляет HTTP-запрос на сервер HTTP.<br/>                                                                                     |
| [**сетаутологонполици**](iwinhttprequest-setautologonpolicy.md)       | Задает текущую [политику автоматического входа в систему](authentication-in-winhttp.md).<br/>                             |
| [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md)   | Выбирает сертификат клиента для отправки на HTTPS-сервер.<br/>                                 |
| [**сеткредентиалс**](iwinhttprequest-setcredentials.md)               | Задает учетные данные для использования с сервером HTTP, прокси-сервером или исходным сервером.<br/>                             |
| [**сетпрокси**](iwinhttprequest-setproxy.md)                           | Задает сведения о прокси-сервере.<br/>                                                                                               |
| [**сетрекуессеадер**](iwinhttprequest-setrequestheader.md)           | Добавляет, изменяет или удаляет заголовок HTTP-запроса.<br/>                                                                            |
| [**сеттимеаутс**](iwinhttprequest-settimeouts.md)                     | Задает отдельные компоненты времени ожидания операции отправки и получения в миллисекундах.<br/>                                   |
| [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md)             | Ожидает завершения асинхронного метода [**Send**](iwinhttprequest-send.md) с необязательным значением времени ожидания в секундах.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **ивинхттпрекуест** имеет следующие свойства.



| Свойство                                                            | Тип доступа           | Описание                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Параметр**](iwinhttprequest-option.md)<br/>                 | Чтение/запись<br/> | Значение параметра WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Только для чтения<br/>  | Тело сущности ответа в виде массива байтов без знака.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Только для чтения<br/>  | Тело сущности ответа в виде [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**респонсетекст**](iwinhttprequest-responsetext.md)<br/>     | Только для чтения<br/>  | Тело объекта ответа.<br/>                                  |
| [**Состояние**](iwinhttprequest-status.md)<br/>                 | Только для чтения<br/>  | Код состояния HTTP из последнего ответа.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Только для чтения<br/>  | Текст состояния HTTP.<br/>                                      |



 

## <a name="remarks"></a>Remarks

Интерфейс **ивинхттпрекуест** , определенный в HttpRequest. idl, реализуется классом с идентификатором **CLSID \_ WinHttpRequest**. Приложение получает этот интерфейс, вызывая [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ WinHttpRequest** и идентификатором интерфейса **IID \_ ивинхттпрекуест**.

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHttp.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивинхттпрекуестевентс**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

