---
description: Компилятор MOF принимает значение с плавающей запятой, указанное для свойства, не допускающего плавающую точку. Значение округляется вверх или вниз и сохраняется как число с неплавающей запятой. Такая ситуация может привести к непредвиденным результатам.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Компиляция MOF-кода со значениями Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265608"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Компиляция MOF-кода со значениями Floating-Point

Компилятор MOF принимает значение с плавающей запятой, указанное для свойства, не допускающего плавающую точку. Значение округляется вверх или вниз и сохраняется как число с неплавающей запятой. Такая ситуация может привести к непредвиденным результатам.

Следующий пример кода MOF определяет класс с именем **ABC** в пространстве имен с именем Test. Этот MOF-код компилируется без ошибок, но нельзя запрашивать значение с плавающей запятой, определенное для свойства **exampleUint16** в экземпляре, создаваемом этим кодом.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Если вы выполните следующий запрос, появится код ошибки, указывающий на недопустимый запрос.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



Однако следующий запрос находит указанный экземпляр.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Компиляция MOF-файлов](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Команды препроцессора](preprocessor-commands.md)
</dt> </dl>

 

 



