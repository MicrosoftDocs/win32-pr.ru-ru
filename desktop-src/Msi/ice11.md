---
description: ICE11 используется с параллельными установками. Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии. Сведения о параллельных установках см. в разделе одновременная установка.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998801"
---
# <a name="ice11"></a>ICE11

ICE11 используется с параллельными установками. Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии. Сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).

## <a name="result"></a>Результат

ICE11 проверяет исходный столбец в [таблице CustomAction](customaction-table.md) для одновременных настраиваемых действий установки. Исходный столбец должен содержать допустимый [GUID](guid.md) (код продукта MSI).

ICE11 отправляет сообщение об ошибке, если исходный столбец таблицы CustomAction создан неправильно для одновременных настраиваемых действий установки.

## <a name="example"></a>Пример

ICE отправляет следующие сообщения об ошибках для приведенного примера.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Таблица свойств](property-table.md) (частичная)



| Свойство        | Значение                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[Таблица CustomAction](customaction-table.md) (частичная)



| CustomAction | Тип | Источник                                 |
|--------------|------|----------------------------------------|
| CA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Чтобы устранить ошибки, для CA1 нельзя выполнить параллельную установку "базового пакета". Это приведет к рекурсивной установке. Эта запись должна быть удалена, либо исходный столбец должен быть изменен на GUID объявленного MSI, который отличается от GUID основного пакета. Для CA2 все символы в верхнем регистре GUID. Наконец, измените исходный столбец CA4's, чтобы он ссылался на допустимый идентификатор GUID объявленного MSI.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Параллельные установки](concurrent-installations.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



