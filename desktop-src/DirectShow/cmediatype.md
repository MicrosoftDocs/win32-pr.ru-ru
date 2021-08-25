---
description: Класс Кмедиатипе управляет типами мультимедиа. Этот класс наследует \_ \_ структуру типа мультимедиа AM. Его можно привести к переменным типа \_ Media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Класс Кмедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49680848fc764cdbbdfeaf3bea363f29427a745297ef4fb39bca09159aa582f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831953"
---
# <a name="cmediatype-class"></a>Класс Кмедиатипе

![Иерархия классов кмедиатипе](images/mtype01.png)

`CMediaType`Класс управляет типами мультимедиа. Этот класс наследует структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Его можно привести к переменным типа **\_ Media \_ Type**.



| Открытые методы                                                      | Описание                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**кмедиатипе**](cmediatype-cmediatype.md)                         | Метод конструктора.                                                            |
| [**~ Кмедиатипе**](cmediatype--cmediatype.md)                       | Метод деструктора.                                                             |
| [**Параметр**](cmediatype-set.md)                                       | Задает тип носителя с другого типа носителя.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Определяет, был ли присвоен основной тип этому объекту.              |
| [**Тип**](cmediatype-type.md)                                     | Извлекает основной тип.                                                      |
| [**сеттипе**](cmediatype-settype.md)                               | Указывает основной тип.                                                      |
| [**Подтип**](cmediatype-subtype.md)                               | Извлекает подтип.                                                         |
| [**сетсубтипе**](cmediatype-setsubtype.md)                         | Указывает подтип.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Определяет, имеют ли образцы фиксированный размер или переменный размер.                |
| [**истемпоралкомпрессед**](cmediatype-istemporalcompressed.md)     | Определяет, использует ли поток временное сжатие.                            |
| [**жетсамплесизе**](cmediatype-getsamplesize.md)                   | Получает размер выборки.                                                     |
| [**сетсамплесизе**](cmediatype-setsamplesize.md)                   | Задает фиксированный размер выборки или указывает, что выборки имеют переменный размер. |
| [**сетвариаблесизе**](cmediatype-setvariablesize.md)               | Указывает, что выборки не имеют фиксированного размера.                               |
| [**сеттемпоралкомпрессион**](cmediatype-settemporalcompression.md) | Указывает, сжимаются ли образцы с использованием временного сжатия.           |
| [**Формат**](cmediatype-format.md)                                 | Получает указатель на блок формата.                                       |
| [**форматленгс**](cmediatype-formatlength.md)                     | Получает длину блока форматирования.                                      |
| [**сетформаттипе**](cmediatype-setformattype.md)                   | Определяет тип формата.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Возвращает тип формата.                                                     |
| [**сетформат**](cmediatype-setformat.md)                           | Задает блок формата.                                                    |
| [**ресетформатбуффер**](cmediatype-resetformatbuffer.md)           | Удаляет блок формата.                                                      |
| [**аллокформатбуффер**](cmediatype-allocformatbuffer.md)           | Выделяет память для блока Format.                                         |
| [**реаллокформатбуффер**](cmediatype-reallocformatbuffer.md)       | Перераспределяет блок формата на новый размер.                                    |
| [**инитмедиатипе**](cmediatype-initmediatype.md)                   | Инициализирует тип мультимедиа.                                                    |
| [**матчеспартиал**](cmediatype-matchespartial.md)                 | Определяет, соответствует ли этот тип носителя частично указанному типу мультимедиа.        |
| [**испартиаллиспеЦифиед**](cmediatype-ispartiallyspecified.md)     | Определяет, определен ли тип мультимедиа частично.                             |
| Операторы                                                           | Описание:                                                                    |
| [**Оператор =**](cmediatype-operator-.md)                          | Перегружает оператор присваивания для копирования типа мультимедиа.                        |
| [**Оператор = =**](cmediatype-operator--.md)                        | Проверяет равенство между объектами `CMediaType`.                               |
| [**operator! =**](cmediatype-operator-neq.md)                      | Проверяет неравенство между объектами `CMediaType`.                             |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




