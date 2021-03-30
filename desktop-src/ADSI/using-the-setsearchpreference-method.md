---
title: Использование метода Сетсеарчпреференце
description: Вызов метода Сетсеарчпреференце IDirectorySearch изменяет способ, которым результаты поиска получаются и предоставляются через интерфейс IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- Сетсеарчпреференце ADSI с помощью метода Сетсеарчпреференце
- ADSI ADSI, пример кода C/C++ с помощью метода Сетсеарчпреференце
- запросы к ADSI с помощью Сетсеарчпреференце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067304"
---
# <a name="using-the-setsearchpreference-method"></a>Использование метода Сетсеарчпреференце

Вызов метода [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) изменяет способ получения и представления результатов поиска через интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Документация по пакету SDK определяет [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) следующим образом:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Можно задать несколько параметров, передав массив в качестве первого параметра и размер массива в качестве второго параметра.


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



В этом примере размер страницы устанавливается в 100 строк, а область — в \_ \_ тип поддерева области объявлений. Параметр размера страницы приводит к тому, что сервер немедленно возвращает данные клиенту после вычисления 100 строк. \_ \_ Параметр поддерева области объявлений определяет, что поиск охватывает все ветви в дереве ниже точки, из которой выполняется поиск.

 

 




