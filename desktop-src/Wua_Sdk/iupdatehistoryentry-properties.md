---
description: Интерфейс Иупдатехисторентри определяет следующие свойства.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Свойства Иупдатехисторентри
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3acdc9ed32c35028a253944d434c23231c5b6d
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2021
ms.locfileid: "105713441"
---
# <a name="iupdatehistoryentry-properties"></a>Свойства Иупдатехисторентри

Интерфейс [**иупдатехисторентри**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) определяет следующие свойства.



| Свойство                                                               | Описание                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Возвращает идентификатор клиентского приложения, которое обработало обновление.                                                  |
| [**Дата**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Возвращает дату и время применения обновления.                                                                        |
| [**Описание**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Возвращает описание обновления.                                                                                       |
| [**Состав**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Возвращает значение **HRESULT** , возвращаемое операцией над обновлением.                                             |
| [**Операция**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Возвращает значение [**символьным**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) , указывающее операцию над обновлением.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Возвращает значение [**оператионресулткоде**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) , указывающее результат операции над обновлением. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Возвращает значение [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) , указывающее, какой сервер предоставил обновление.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Возвращает идентификатор службы обновления, не являющийся обновлением Windows.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Возвращает гиперссылку на сведения о поддержке для конкретного языка для обновления.                                             |
| [**Заголовок**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Возвращает название обновления.                                                                                             |
| [**унинсталлатионнотес**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Возвращает заметки об удалении обновления.                                                                              |
| [**унинсталлатионстепс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Возвращает интерфейс [**истрингколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) , содержащий шаги удаления для обновления.  |
| [**унмаппедресулткоде**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Возвращает Несопоставленный код результата, возвращаемый операцией в обновлении.                                           |
| [**упдатеидентити**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Возвращает строку. Строка содержит уникальный идентификатор обновления.                                                   |



 

 

 
