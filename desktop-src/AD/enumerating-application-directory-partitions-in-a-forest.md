---
title: Перечисление разделов каталога приложений в лесу
description: Как и разделы домена, каждый раздел каталога приложений представляется объектом crossRef в контейнере разделов раздела конфигурации.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Перечисление разделов каталога приложений в лесу AD
- Разделы каталога приложений AD, перечисление в лесу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069775"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Перечисление разделов каталога приложений в лесу

Как и разделы домена, каждый раздел каталога приложений представляется объектом [**crossRef**](/windows/desktop/ADSchema/c-crossref) в контейнере разделов раздела конфигурации. Каждый объект **crossRef** хранит данные о соответствующей секции.

Объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , представляющий раздел домена, отличается от объекта **crossRef** , который представляет раздел каталога приложения по содержимому атрибута [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Объект **crossRef** , представляющий раздел домена, будет содержать флаги [**AD \_ системфлаг \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) и **ADS \_ системфлаг \_ CR \_ NTDS \_** , заданные в атрибуте **systemFlags** . Объект **crossRef** , представляющий раздел каталога приложений, будет иметь флаг **ADS \_ системфлаг \_ CR \_ NTDS \_ NC** , а флаг AD **\_ Системфлаг \_ CR \_ NTDS \_ domain** не будет установлен в атрибуте **systemFlags** .

Для объектов [**crossRef**](/windows/desktop/ADSchema/c-crossref) , представляющих разделы схемы и конфигурации, также будет установлен флаг On [**ADS \_ системфлаг \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) , а флаг **AD \_ Системфлаг \_ CR \_ NTDS \_ domain** не будет установлен в атрибуте [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Для этого эти два объекта **crossRef** должны быть различны по содержимому атрибута [**NCName**](/windows/desktop/ADSchema/a-ncname) . Атрибут **NCName** для объекта **crossRef** , представляющего контейнер схемы, будет идентичен атрибуту **счеманамингконтекст** объекта RootDSE. Аналогичным образом атрибут **NCName** для объекта **crossRef** , представляющего контейнер конфигурации, будет совпадать с атрибутом **конфигуратионнамингконтекст** объекта RootDSE.

**Чтобы найти все разделы каталога приложений в лесу, выполните следующие действия.**

1.  В контейнере секции раздела конфигурации найдите или перечислите все объекты [**crossRef**](/windows/desktop/ADSchema/c-crossref) .
2.  Если у объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) нет установленного флага [**ADS \_ системфлаг \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) или в значении атрибута [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) установлен флаг **\_ домена ADS системфлаг \_ CR \_ NTDS \_** , исключите объект из результирующего набора.
3.  Исключите секцию схемы из результирующего набора, сравнив атрибут [**NCName**](/windows/desktop/ADSchema/a-ncname) объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) с атрибутом **счеманамингконтекст** объекта RootDSE.
4.  Исключите раздел конфигурации из результирующего набора, сравнив атрибут [**NCName**](/windows/desktop/ADSchema/a-ncname) объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) с атрибутом **конфигуратионнамингконтекст** объекта RootDSE.
5.  Остальные объекты [**crossRef**](/windows/desktop/ADSchema/c-crossref) в результирующем наборе представляют разделы каталога приложений.

 

 