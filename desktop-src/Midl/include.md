---
title: include attribute
description: Инструкция ACF include указывает один или несколько файлов заголовков, которые будут включены в созданный код-заглушку.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- включить атрибут MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133106"
---
# <a name="include-attribute"></a>include attribute

Инструкция ACF **include** указывает один или несколько файлов заголовков, которые будут включены в созданный код-заглушку.

``` syntax
include filenames;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имена файлов* 
</dt> <dd>

Указывает имя одного или нескольких файлов заголовков языка C. Используйте полное имя файла, включая. Расширение H и заключите каждое имя файла в кавычки. Разделяйте имена файлов заголовков языка C запятыми.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В результате выполнения инструкции **include** созданный код-заглушка будет содержать инструкцию C-препроцессор **\# include** . При компиляции заглушек вы предоставляете заголовочный файл языка C. Инструкции include используют механизм поиска в структуре каталогов для включенных файлов.

> [!Note]  
> Используйте директиву [**Import**](import.md) вместо директивы **include** для системных файлов, содержащих типы данных, которые необходимо сделать доступными для IDL-файла. Директива **Import** игнорирует прототипы функций и позволяет использовать параметры компилятора MIDL, которые оптимизируют создание подпрограмм поддержки.

 

## <a name="examples"></a>Примеры

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**импортиру**](import.md)
</dt> <dt>

[Импорт файлов и библиотек типов](importing-files-and-type-libraries.md)
</dt> <dt>

[Импорт системных файлов заголовков](importing-system-header-files.md)
</dt> </dl>

 

 




