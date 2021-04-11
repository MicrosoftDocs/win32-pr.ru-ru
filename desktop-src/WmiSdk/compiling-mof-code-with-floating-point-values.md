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
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="99d72-105">Компиляция MOF-кода со значениями Floating-Point</span><span class="sxs-lookup"><span data-stu-id="99d72-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="99d72-106">Компилятор MOF принимает значение с плавающей запятой, указанное для свойства, не допускающего плавающую точку.</span><span class="sxs-lookup"><span data-stu-id="99d72-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="99d72-107">Значение округляется вверх или вниз и сохраняется как число с неплавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="99d72-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="99d72-108">Такая ситуация может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="99d72-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="99d72-109">Следующий пример кода MOF определяет класс с именем **ABC** в пространстве имен с именем Test.</span><span class="sxs-lookup"><span data-stu-id="99d72-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="99d72-110">Этот MOF-код компилируется без ошибок, но нельзя запрашивать значение с плавающей запятой, определенное для свойства **exampleUint16** в экземпляре, создаваемом этим кодом.</span><span class="sxs-lookup"><span data-stu-id="99d72-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

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

<span data-ttu-id="99d72-111">Если вы выполните следующий запрос, появится код ошибки, указывающий на недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="99d72-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="99d72-112">Однако следующий запрос находит указанный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="99d72-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="99d72-113">См. также</span><span class="sxs-lookup"><span data-stu-id="99d72-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d72-114">Компиляция MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="99d72-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="99d72-115">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="99d72-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="99d72-116">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="99d72-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



