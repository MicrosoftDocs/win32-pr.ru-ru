---
description: Следующие методы определяются интерфейсом Иокспадмин. Методы доступа к свойствам не показаны здесь. Сведения о свойствах Иокспадмин см. в разделе Свойства Иокспадмин.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Методы Иокспадмин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a455ae5cfbb49d60cc0d0a03265d05c98efa2f2217746086b0acf0a4230709dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992854"
---
# <a name="methods-of-iocspadmin"></a>Методы Иокспадмин

Следующие методы определяются интерфейсом [**иокспадмин**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) . Методы доступа к свойствам не показаны здесь. Сведения о свойствах **иокспадмин** см. в разделе [Свойства иокспадмин](properties-of-iocspadmin.md).



| Метод                                                              | Описание                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Подключается к серверу ответчика Online Certificate Status Protocol (OCSP) и инициализирует объект **окспадмин** с данными конфигурации с сервера.                                                                                                     |
| [**жесашалгорисмс**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Возвращает список имен хэш-алгоритма. Сервер респондента использует один из именованных алгоритмов для подписи ответов OCSP для определенной конфигурации [*центра сертификации*](../secgloss/c-gly.md) (ЦС). |
| [**жетмиролес**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Получает маску доступа для ролей привилегий для пользователя на данном сервере респондента.                                                                                                                                                                                           |
| [**Безопасность**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Возвращает сведения о дескрипторе безопасности для сервера респондента.                                                                                                                                                                                                              |
| [**жетсигнингцертификатес**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Возвращает сертификаты подписи, доступные на сервере респондента для данного сертификата ЦС.                                                                                                                                                                        |
| [**Проверка связи**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Проверяет DCOM-подключение к службе респондента.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Обновляет службу ответчика с изменениями конфигурации.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Обновляет сведения о дескрипторе безопасности для сервера ответчика OCSP.                                                                                                                                                                                                     |



 

 

 
