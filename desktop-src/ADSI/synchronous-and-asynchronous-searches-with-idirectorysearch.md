---
title: Синхронный и асинхронный поиск с помощью IDirectorySearch
description: При выполнении поиска с помощью интерфейса IDirectorySearch метод IDirectorySearch ExecuteSearch не отправляет запрос на поиск на сервер.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Синхронный и асинхронный поиск с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, синхронный и асинхронный поиск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3891351bc7ebb9872938f3022f5397100e0be74ca6cd2d86d21a2535f010cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690201"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Синхронный и асинхронный поиск с помощью IDirectorySearch

При выполнении поиска с помощью интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) метод [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) не отправляет запрос на поиск на сервер. Этот метод сохраняет только параметры поиска. Запрос на поиск фактически отправляется при вызове [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

При поиске Active Directory основное различие между синхронным и асинхронным — при возвращении первой строки результата, то есть при возврате первого вызова [**жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .

В синхронном поиске, если разбиение по страницам не включено, первая строка возвращается, когда сервер конструирует и возвращает клиенту весь результирующий набор. Если разбиение по страницам включено, первая строка возвращается при возвращении первой страницы результирующего набора.

При асинхронном поиске, если разбиение по страницам не включено, первая строка возвращается при создании сервером первой строки результирующего набора. Если разбиение по страницам включено, первая строка возвращается при возвращении первой страницы результирующего набора.

Тип поиска по умолчанию — синхронный. Чтобы указать асинхронный поиск, установите параметр **ADS \_ сеарчпреф \_ асинхронного** поиска с **адстипе \_ логическим** значением **true** в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Эта операция показана в следующем примере кода.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




