---
description: в этом разделе описываются системные константы, перечисления и флаги свойств Windows.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: константы, перечисления и флаги (система свойств Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718213"
---
# <a name="constants-enumerations-and-flags"></a>Константы, перечисления и флаги

в этом разделе описываются системные константы, перечисления и флаги свойств Windows.



| Раздел                                                                              | Содержимое                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетпропертисторефлагс**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Указывает флаги, которые изменяют объект хранилища свойств, извлеченный методами, которые создают хранилище свойств, например [**IShellItem2:: жетпропертисторе**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) или [**Ипропертисторефактори:: жетпропертисторе**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**пдопстатус**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Предоставляет флаги состояния операции.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_Флаги pKa**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Описывает поведение массива изменения свойств.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_тип агрегирования пропдеск \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Описывает, как значения свойств отображаются при выборе нескольких элементов. Для конкретного свойства \_ тип агрегирования пропдеск \_ описывает, как должно отображаться свойство, если выбрано несколько элементов со значением свойства, например, должны ли значения суммироваться или выводиться в среднем или просто отображаться со строкой по умолчанию "несколько значений".<br/> |
| [**\_тип COLUMNINDEX \_ пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Указывает, можно ли индексировать свойство.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_тип условия \_ пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | описывает тип условия, используемого при отображении свойства в пользовательском интерфейсе построителя запросов в Windows Vista, но не в Windows 7 и более поздних версиях.<br/>                                                                                                                                                                                                                                      |
| [**ПРОПДЕСК \_ енумфилтер**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Описывает отфильтрованный список возвращаемых описаний свойств.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_ \_ флаги формата пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Используется вспомогательными функциями описания свойств, например [**псформатфордисплай**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), для указания формата строки свойства.<br/>                                                                                                                                                                                                                         |
| [**\_тип РЕЛАТИВЕДЕСКРИПТИОН \_ пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Описывает тип относительного описания для описания свойства, как определено атрибутом *релативедескриптионтипе* элемента [displayInfo](./propdesc-schema-displayinfo.md) .<br/>                                                                                                                                                                                   |
| [**\_ \_ Флаги сеарчинфо пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | определяет, индексируется ли свойство с помощью Windows поиска.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_ \_ Флаги типа пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Описывает атрибуты элемента [typeInfo](./propdesc-schema-typeinfo.md) в файле. пропдеск свойства.<br/>                                                                                                                                                                                                                                                                |
| [**\_ \_ Флаги представления пропдеск**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Эти флаги описывают свойства в строках списка описания свойств.<br/>                                                                                                                                                                                                                                                                                                           |
| [**\_Флаги пропертюи**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Задает функции свойств.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**\_модуль сравнения \_ пропвар**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Эти флаги связаны с определенными [**пропвариантми**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) структурными сравнениями.<br/>                                                                                                                                                                                                                                                                               |
| [**\_состояние PSC**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Задает состояние свойства. Они задаются вручную кодом, в котором размещается кэш хранилища свойств в памяти.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства Windows](props.md)
</dt> <dt>

[Схема описания свойства](property-description-schema.md)
</dt> <dt>

[Наборы свойств](property-sets.md)
</dt> <dt>

[Интерфейсы](interfaces.md)
</dt> <dt>

[Функции](functions.md)
</dt> <dt>

[Структуры](structures.md)
</dt> </dl>

 

 
