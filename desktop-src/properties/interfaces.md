---
description: в этом разделе описываются интерфейсы системы свойств Windows.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: интерфейсы (система свойств Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d608e1b994541667847d755e95966b6ea2770c2d0c73ce86ef8fbd79b8c9dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600124"
---
# <a name="interfaces-windows-property-system"></a>интерфейсы (система свойств Windows)

в этом разделе описываются интерфейсы системы свойств Windows.



| Раздел                                                                                        | Содержимое                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ипропертичанже**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Предоставляет метод, инкапсулирующий изменение в отдельном свойстве.                                                                                                                                                                                                                                                                                                                          |
| [**ипропертичанжеаррай**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Предоставляет методы для нескольких операций изменения, которые могут быть переданы в [**интерфейс IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation).                                                                                                                                                                                                                                                                   |
| [**ипропертидескриптион**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Предоставляет методы, которые перечисляют и извлекают сведения об описании отдельных свойств.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Предоставляет методы, которые перечисляют и извлекают сведения об описании отдельных свойств.                                                                                                                                                                                                                                                                                                       |
| [**ипропертидескриптионалиасинфо**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Предоставляет методы для получения свойств "Sorting" столбцов элемента. Этот интерфейс используется объектами пользовательского интерфейса, которые хотят получить первичные или вторичные столбцы сортировки для данного свойства.                                                                                                                                                                                                |
| [**ипропертидескриптионлист**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Предоставляет методы, которые извлекают сведения из коллекции описаний свойств, представленных в виде списка.                                                                                                                                                                                                                                                                                   |
| [**ипропертидескриптионрелатедпропертинфо**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Предоставляет метод, Извлекает интерфейс [**ипропертидескриптион**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                       |
| [**ипропертидескриптионсеарчинфо**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Предоставляет сведения, связанные с поиском для свойства. Сведения, предоставляемые этим интерфейсом, берутся из схемы [пропертидескриптион](./propdesc-schema-propertydescription.md) , элемента [сеарчинфо](./propdesc-schema-searchinfo.md) для данного свойства. эти сведения используются индексатором поиска Windows. Большинству вызывающих приложений не требуется вызывать этот интерфейс. |
| [**ипропертенумтипе**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Предоставляет методы, которые извлекают данные из сведений о перечислении. [**Ипропертенумтипе**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) предоставляет доступ к элементам [enum](./propdesc-schema-enum.md) и [енумранже](./propdesc-schema-enumrange.md) в [схеме свойств](./propdesc-schema-entry.md) программным способом во время выполнения.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Предоставляет методы, которые извлекают данные из сведений о перечислении. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) расширяет [**ипропертенумтипе**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**ипропертенумтипелист**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Предоставляет методы для перечисления возможных значений свойства.                                                                                                                                                                                                                                                                                                                         |
| [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Предоставляет методы для перечисления, получения и установки значений свойств.                                                                                                                                                                                                                                                                                                                     |
| [**ипропертисторекаче**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Предоставляет методы, позволяющие обработчику управлять различными состояниями для каждого свойства.                                                                                                                                                                                                                                                                                                           |
| [**ипропертисторекапабилитиес**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Предоставляет метод, определяющий, может ли пользователь изменять свойство в пользовательском интерфейсе.                                                                                                                                                                                                                                                                                                   |
| [**ипропертисторефактори**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Предоставляет методы для получения объекта [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .                                                                                                                                                                                                                                                                                                               |
| [**ипропертисистем**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Предоставляет методы для получения описаний свойств, регистрации и отмены регистрации схем свойств, перечисления описаний свойств и форматирования значений свойств строго определенным образом.                                                                                                                                                                                                                |
| [**ипропертюи**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Вместо этого разработчики должны использовать [**ипропертидескриптион**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства Windows](props.md)
</dt> <dt>

[Схема описания свойства](property-description-schema.md)
</dt> <dt>

[Наборы свойств](property-sets.md)
</dt> <dt>

[Функции](functions.md)
</dt> <dt>

[Структуры](structures.md)
</dt> <dt>

[Константы, перечисления и флаги](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
