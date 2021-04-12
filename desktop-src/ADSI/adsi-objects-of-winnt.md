---
title: Объекты ADSI в WinNT
description: Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Службы WinNT Service Provider ADSI, объекты ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132814"
---
# <a name="adsi-objects-of-winnt"></a>Объекты ADSI в WinNT

Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Объект ADSI</th>
<th>Описание</th>
<th>Поддерживаемые интерфейсы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Класс</strong></td>
<td>Объект ADSI, представляющий определение класса.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>иадскласс</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Компьютер</strong></td>
<td>Объект ADSI, представляющий компьютер.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>иадскомпутер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>иадскомпутероператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Доменная</strong></td>
<td>Объект ADSI, представляющий домен по сети.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>иадсдомаин</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>Объект ADSI, представляющий файловую службу.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Объект ADSI, представляющий общую папку.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>фпнвфилесервице</strong></td>
<td>Объект ADSI, представляющий файловую службу.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>фпнвфилешаре</strong></td>
<td>Объект ADSI, представляющий общую папку.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>фпнвресаурце</strong></td>
<td>Объект ADSI, представляющий ресурс.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>фпнвресаурцесколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию ресурсов.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></td>
</tr>
<tr class="even">
<td><strong>фпнвсессион</strong></td>
<td>Объект ADSI, представляющий сеанс.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>фпнвсессионсколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию сеансов.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></td>
</tr>
<tr class="even">
<td><strong>Группа</strong></td>
<td>Объект ADSI, представляющий группу.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
Параметр-info не может использоваться для групп, содержащих члены, которые являются wellKnown субъектами безопасности в области WinNT.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>Объект ADSI, представляющий коллекцию групп.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>иадсмемберс</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Локальная группа</strong></td>
<td>Объект ADSI, представляющий локальную группу.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>локалграупколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию локальных групп.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>иадсмемберс</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Пространство имен</strong></td>
<td>Объект ADSI, представляющий пространство имен WinNT.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>иадсопендсобжект</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>PrintJob</strong></td>
<td>Объект ADSI, представляющий задание печати.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>иадспринтжоб</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>иадспринтжобоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>принтжобсколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию заданий печати.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Объект ADSI, представляющий очередь печати.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>иадспринткуеуе</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>иадспринткуеуеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Свойство</strong></td>
<td>Объект ADSI, представляющий определение атрибута.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>иадспроперти</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Ресурс</strong></td>
<td>Объект ADSI, представляющий ресурс.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>ресаурцесколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию ресурсов.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Схема</strong></td>
<td>Объект ADSI, представляющий контейнер схемы.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>иадсконтаинер</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Служба</strong></td>
<td>Объект ADSI, представляющий службу.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>иадссервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>иадссервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Session</strong></td>
<td>Объект ADSI, представляющий сеанс.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>сессионсколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию сеансов.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Синтаксис</strong></td>
<td>Объект ADSI, представляющий синтаксис атрибута.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>иадссинтакс</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Пользователь</strong></td>
<td>Объект ADSI, представляющий учетную запись пользователя.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>усерграупколлектион</strong></td>
<td>Объект ADSI, представляющий коллекцию групп пользователей.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>иадсмемберс</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





