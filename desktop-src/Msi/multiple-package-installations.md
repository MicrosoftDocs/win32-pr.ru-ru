---
description: Windows Установщик может устанавливать несколько пакетов с помощью обработки транзакций.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943415"
---
# <a name="multiple-package-installations"></a>Multiple-Package установки

Windows Установщик может устанавливать несколько пакетов с помощью [*обработки транзакций*](t-gly.md). эта возможность доступна начиная с установщик Windows 4,5. Установщик установит все пакеты, относящиеся к транзакции с несколькими пакетами или ни одному из пакетов. если не удается успешно установить все пакеты в транзакции или пользователь отменяет установку, установщик Windows может откатить изменения и восстановить состояние компьютера в исходном состоянии.

Пакет установки с несколькими пакетами может содержать [таблицу мсиембеддедчаинер](msiembeddedchainer-table.md) , которая ссылается на определяемую пользователем функцию, которая использует [**функции мсибегинтрансактион**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**мсижоинтрансактион**](/windows/desktop/api/Msi/nf-msi-msijointransaction)и [**мсиендтрансактион**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

В [таблице мсипаккажецертификате](msipackagecertificate-table.md) перечислены сертификаты цифровых подписей, используемые для проверки подлинности пакетов установки, которые делают установку нескольких пакетов. С помощью этой таблицы можно сократить количество случаев, когда в многопакетной установке отображается запрос контроля [*учетных записей*](u-gly.md) (UAC), требующий ответ администратором.

следующие установщик Windows функции могут вносить изменения на компьютер пользователя, когда установщик Windows устанавливает, восстанавливает, обновляет или удаляет приложения. начиная с установщик Windows 4,5, установщик может откатить изменения, внесенные этими функциями, во время [*обработки транзакций*](t-gly.md) многопакетной установки.

<dl>

[**мсиадвертисепродукт**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**мсиконфигурепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**мсиинсталлмиссингкомпонент**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**мсипровидекуалифиедкомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**мсипровидекуалифиедкомпонентекс**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**мсиреинсталлфеатуре**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

существует исключение, если установщик Windows встречает пакет, принадлежащий многопакетной установке, содержащей действие [форцеребут](forcereboot-action.md) или [счедулеребут](schedulereboot-action.md) . в этом случае установщик Windows не устанавливает только этот пакет. Можно установить другие пакеты, принадлежащие многопакетной установке, которые не содержат действие Форцеребут или Счедулеребут.

**[установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md): * *[*обработка транзакций*](t-gly.md) для многопакетных установщик Windows установок не поддерживается. этим версиям установщик Windows не удается выполнить откат установки нескольких пакетов в рамках одной транзакции.

**Windows Server 2008 R2 с включенной ролью [службы удаленных рабочих столов](../termserv/terminal-services-portal.md) :** Не поддерживается. Если роль [службы удаленных рабочих столов](../termserv/terminal-services-portal.md) включена, то установка нескольких пакетов с помощью [таблицы мсиембеддедчаинер](msiembeddedchainer-table.md) завершается ошибкой.

 

 
