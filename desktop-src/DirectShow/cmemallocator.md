---
description: Реализует распределитель, который поддерживает интерфейс Имемаллокатор.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Класс Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915934"
---
# <a name="cmemallocator-class"></a>Класс Кмемаллокатор

![Иерархия классов кмемаллокатор](images/filter10.png)

Реализует распределитель, который поддерживает интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Этот класс является производным от [**кбасеаллокатор**](cbaseallocator.md). Дополнительные сведения о распределителях см. в документации по [**кбасеаллокатор**](cbaseallocator.md).



| Защищенные переменные членов                              | Описание                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pBuffer**](cmemallocator-m-pbuffer.md)           | Указатель на блок памяти, содержащий буферы.                   |
| Защищенные методы                                       | Описание                                                              |
| [**Free**](cmemallocator-free.md)                      | Метод заполнителя; вызывается во время операции дефиксации.                  |
| [**реаллифри**](cmemallocator-reallyfree.md)          | Освобождает память для буферов.                                     |
| [**Идентификатор**](cmemallocator-alloc.md)                    | Выделяет память для буферов.                                        |
| Открытые методы                                          | Описание                                                              |
| [**кмемаллокатор**](cmemallocator-cmemallocator.md)    | Метод конструктора.                                                      |
| [**~ Кмемаллокатор**](cmemallocator--cmemallocator.md) | Метод деструктора.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Создает новый экземпляр класса **кмемаллокатор** .                   |
| Методы Имемаллокатор                                   | Описание                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Указывает количество выделяемых буферов и размер каждого буфера. |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Предоставление пользовательского распределителя](providing-a-custom-allocator.md)
</dt> </dl>

 

 




