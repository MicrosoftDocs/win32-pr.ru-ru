---
title: Функции ADSI
description: Active Directory интерфейсы служб предоставляют следующие вспомогательные функции клиентам, которые не используют автоматизацию.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI ADSI, ссылки, функции
- функции ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328443"
---
# <a name="adsi-functions"></a>Функции ADSI

Active Directory интерфейсы служб предоставляют следующие вспомогательные функции клиентам, которые не используют автоматизацию.



| Функция                                           | Описание                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Создает объект перечислителя для указанного объекта контейнера ADSI.                              |
| [**адсбуилдвараррайинт**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Создает массив вариантов из массива **DWORD** s.                                                |
| [**адсбуилдвараррайстр**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Создает массив Variant из массива строк в Юникоде.                                           |
| [**адсенкодебинаридата**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Преобразует большой двоичный объект двоичных данных в формат, подходящий для фильтра поиска.                         |
| [**адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Заполняет массив Variant элементами, полученными из указанного объекта перечислителя.            |
| [**адсфриенумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Освобождает объект перечислителя, созданный ранее [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator). |
| [**адсжетластеррор**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Извлекает Последнее значение кода ошибки вызывающего потока.                                         |
| [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Выполняет привязку к объекту ADSI, используя текущие учетные данные.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Выполняет привязку к объекту ADSI с использованием указанных учетных данных                                                |
| [**адссетластеррор**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Задает значение кода ошибки вызывающего потока.                                                   |
| [**аллокадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Выделяет блок памяти.                                                                       |
| [**аллокадсстр**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Выделяет память для заданной строки.                                                               |
| [**фриадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Освобождает память, выделенную [**аллокадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).                                  |
| [**фриадсстр**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Освобождает память, выделенную для заданной строки.                                                   |
| [**реаллокадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Назначает существующее содержимое памяти только что созданному расположению в памяти.                            |
| [**реаллокадсстр**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Заменяет существующую строку новой.                                                        |



 

Следующие функции ADSI устарели.



| Функция                                                  | Описание |
|-----------------------------------------------------------|-------------|
| [**адсфриаллерроррекордс**](obsolete-adsi-functions.md) | Является устаревшей.   |
| [**адсдекодебинаридата**](obsolete-adsi-functions.md)    | Является устаревшей.   |
| [**пропварианттоадстипе**](obsolete-adsi-functions.md)   | Является устаревшей.   |
| [**адстипетопропвариант**](obsolete-adsi-functions.md)   | Является устаревшей.   |
| [**адсфриадсвалуес**](obsolete-adsi-functions.md)       | Является устаревшей.   |
| [**инитадсмем**](obsolete-adsi-functions.md)             | Является устаревшей.   |
| [**ассертадсмемлеакс**](obsolete-adsi-functions.md)      | Является устаревшей.   |
| [**думпмеморитраккер**](obsolete-adsi-functions.md)      | Является устаревшей.   |



 

 

 




