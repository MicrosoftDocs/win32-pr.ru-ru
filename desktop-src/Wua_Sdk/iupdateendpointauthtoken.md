---
description: Предоставляет методы, которые WUA может использовать для сбора сведений о маркере конечной точки.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Интерфейс Иупдатиндпоинтаустокен (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497607"
---
# <a name="iupdateendpointauthtoken-interface"></a>Интерфейс Иупдатиндпоинтаустокен

Предоставляет методы, которые WUA может использовать для сбора сведений о маркере конечной точки.

## <a name="members"></a>Элементы

Интерфейс **иупдатиндпоинтаустокен** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иупдатиндпоинтаустокен** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иупдатиндпоинтаустокен** содержит следующие методы.



| Метод                                                                                | Описание                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Возвращает идентификатор службы для проверки подлинности.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Возвращает ключ, используемый для подписывания исходящих сообщений между клиентским компьютером и серквице.<br/>                        |
| [**токендата**](iupdateendpointauthtoken-tokendata.md)                               | Возвращает XML-данные (переданные по каналу передачи), представляющие токен. <br/>                                               |
| [**токенреференцеаттачед**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Возвращает XML-формат присоединенной ссылки на токен.<br/>                                                       |
| [**токенреференцеунаттачед**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Возвращает XML-формат неприсоединенной ссылки на токен.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Возвращает тип маркера конечной точки, например маркер WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1. <br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                   |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                |
| Header<br/>                   | <dl> <dt>Упдатиндпоинтаус. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Упдатиндпоинтаус. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Упдатиндпоинтаус. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
