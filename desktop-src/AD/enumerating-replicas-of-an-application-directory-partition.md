---
title: Перечисление реплик раздела каталога приложений
description: В этом разделе показано, как перечислить реплики для раздела каталога приложений.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Перечисление реплик раздела каталога приложений (AD)
- Разделы каталога приложений AD, перечисление реплик
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987343"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Перечисление реплик раздела каталога приложений

При добавлении реплики раздела каталога приложений различающееся имя объекта [**нтдсдса**](/windows/desktop/ADSchema/c-ntdsdsa) для контроллера домена, который будет содержать реплику, добавляется в атрибут [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Используемый объект **crossRef** представляет раздел каталога приложения.

**Перечисление реплик для раздела каталога приложений**

1.  Найдите в контейнере секций объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , имеющий значение атрибута [**NCName**](/windows/desktop/ADSchema/a-ncname) , равное различающихся именам разделов каталога приложений.
2.  Используйте каждое значение атрибута [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) для привязки к объекту [**нтдсдса**](/windows/desktop/ADSchema/c-ntdsdsa) сервера.
3.  Получите значение ADsPath для родителя каждого объекта [**нтдсдса**](/windows/desktop/ADSchema/c-ntdsdsa) . Это объект, представляющий сервер контроллера домена. Используйте путь ADsPath для привязки к объекту сервера.
4.  Получите значение атрибута [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) объекта Server. Это свойство с одним значением, которое содержит DNS-имя сервера.

Из-за задержки репликации и запланированных задержек запуска KCC возможно, что фактические активные реплики для раздела каталога приложений могут не соответствовать списку контроллеров домена, указанному атрибутом [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Более точный, но менее эффективный способ определения фактических активных реплик раздела каталога приложений заключается в поиске всех объектов [**нтдсдса**](/windows/desktop/ADSchema/c-ntdsdsa) в лесу, имеющих атрибут [**msDS-хасмастернкс**](/windows/desktop/ADSchema/a-msds-hasmasterncs) , который содержит различающееся имя раздела каталога приложений. Атрибут **msDS-хасмастернкс** содержит отличительные имена всех доступных для записи разделов каталога, содержащихся в контроллере домена, включая разделы каталога приложений.

 

 