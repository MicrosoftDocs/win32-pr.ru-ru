---
description: Объект данных имеет следующее определение синтаксиса.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Данные (формат файла X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a520d05571f592243e71799ad21a7da3a8d8bea6a3f5819508a194eaca90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986004"
---
# <a name="data-x-file-format-binary-encoding"></a>Данные (формат файла X, двоичное кодирование)

Объект данных имеет следующее определение синтаксиса.


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



Обратите внимание, что в \_ списке число и данные с плавающей запятой \_ в двоичных файлах \_ не используются разделители и \_ точка с запятой маркера. Запятая и точка с запятой используются в \_ данных списка строк. Также обратите внимание, что можно использовать только \_ ссылку на данные для необязательных элементов данных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Двоичное кодирование](binary-encoding.md)
</dt> </dl>

 

 



