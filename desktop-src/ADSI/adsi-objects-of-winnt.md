---
title: Объекты ADSI в WinNT
description: Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Службы WinNT Service Provider ADSI, объекты ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f3d2cb845e7fa6c754198abbb9a274987f69a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467391"
---
# <a name="adsi-objects-of-winnt"></a>Объекты ADSI в WinNT

Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.




| Объект ADSI | Описание | Поддерживаемые интерфейсы | 
|-------------|-------------|----------------------|
| <strong>Класс</strong> | Объект ADSI, представляющий определение класса. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>иадскласс</strong></a></dt></dl> | 
| <strong>Компьютер</strong> | Объект ADSI, представляющий компьютер. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>иадскомпутер</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>иадскомпутероператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>Доменная</strong> | Объект ADSI, представляющий домен по сети. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>иадсдомаин</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>FileService</strong> | Объект ADSI, представляющий файловую службу. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>FileShare</strong> | Объект ADSI, представляющий общую папку. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>фпнвфилесервице</strong> | Объект ADSI, представляющий файловую службу. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt></dl> | 
| <strong>фпнвфилешаре</strong> | Объект ADSI, представляющий общую папку. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>фпнвресаурце</strong> | Объект ADSI, представляющий ресурс. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>фпнвресаурцесколлектион</strong> | Объект ADSI, представляющий коллекцию ресурсов. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a> | 
| <strong>фпнвсессион</strong> | Объект ADSI, представляющий сеанс. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>фпнвсессионсколлектион</strong> | Объект ADSI, представляющий коллекцию сеансов. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a> | 
| <strong>Группа</strong> | Объект ADSI, представляющий группу. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl><blockquote>[!Note]<br />Параметр-info не может использоваться для групп, содержащих члены, которые являются wellKnown субъектами безопасности в области WinNT.</blockquote><br /> | 
| <strong>GroupCollection</strong> | Объект ADSI, представляющий коллекцию групп. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>иадсмемберс</strong></a></dt></dl> | 
| <strong>Локальная группа</strong> | Объект ADSI, представляющий локальную группу. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>локалграупколлектион</strong> | Объект ADSI, представляющий коллекцию локальных групп. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>иадсмемберс</strong></a></dt></dl> | 
| <strong>Пространство имен</strong> | Объект ADSI, представляющий пространство имен WinNT. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>иадсопендсобжект</strong></a></dt></dl> | 
| <strong>PrintJob</strong> | Объект ADSI, представляющий задание печати. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>иадспринтжоб</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>иадспринтжобоператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>принтжобсколлектион</strong> | Объект ADSI, представляющий коллекцию заданий печати. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a> | 
| <strong>PrintQueue</strong> | Объект ADSI, представляющий очередь печати. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>иадспринткуеуе</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>иадспринткуеуеоператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>Свойство</strong> | Объект ADSI, представляющий определение атрибута. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>иадспроперти</strong></a></dt></dl> | 
| <strong>Ресурс</strong> | Объект ADSI, представляющий ресурс. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>ресаурцесколлектион</strong> | Объект ADSI, представляющий коллекцию ресурсов. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a> | 
| <strong>Схема</strong> | Объект ADSI, представляющий контейнер схемы. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt></dl> | 
| <strong>Служба</strong> | Объект ADSI, представляющий службу. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>иадссервице</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>иадссервицеоператионс</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>Session</strong> | Объект ADSI, представляющий сеанс. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>сессионсколлектион</strong> | Объект ADSI, представляющий коллекцию сеансов. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a> | 
| <strong>Синтаксис</strong> | Объект ADSI, представляющий синтаксис атрибута. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>иадссинтакс</strong></a></dt></dl> | 
| <strong>Пользователь</strong> | Объект ADSI, представляющий учетную запись пользователя. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt></dl> | 
| <strong>усерграупколлектион</strong> | Объект ADSI, представляющий коллекцию групп пользователей. | <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>иадсмемберс</strong></a> | 




 

 

 





