---
description: Объект данных имеет следующее определение синтаксиса.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Данные (формат файла X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139230"
---
# <a name="data-x-file-format-binary-encoding"></a><span data-ttu-id="b0914-103">Данные (формат файла X, двоичное кодирование)</span><span class="sxs-lookup"><span data-stu-id="b0914-103">Data (X file format, binary encoding)</span></span>

<span data-ttu-id="b0914-104">Объект данных имеет следующее определение синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="b0914-104">A data object has the following syntax definition.</span></span>


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



<span data-ttu-id="b0914-105">Обратите внимание, что в \_ списке число и данные с плавающей запятой \_ в двоичных файлах \_ не используются разделители и \_ точка с запятой маркера.</span><span class="sxs-lookup"><span data-stu-id="b0914-105">Note that in number\_list and float\_list data in binary files, TOKEN\_COMMA and TOKEN\_SEMICOLON are not used.</span></span> <span data-ttu-id="b0914-106">Запятая и точка с запятой используются в \_ данных списка строк.</span><span class="sxs-lookup"><span data-stu-id="b0914-106">The comma and semicolon are used in string\_list data.</span></span> <span data-ttu-id="b0914-107">Также обратите внимание, что можно использовать только \_ ссылку на данные для необязательных элементов данных.</span><span class="sxs-lookup"><span data-stu-id="b0914-107">Also note that you can only use data\_reference for optional data members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0914-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b0914-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0914-109">Двоичное кодирование</span><span class="sxs-lookup"><span data-stu-id="b0914-109">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



