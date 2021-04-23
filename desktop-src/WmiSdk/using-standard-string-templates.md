---
description: Несколько потребителей, например потребитель событий активных скриптов или потребитель событий командной строки, имеют свойства строки с квалификатором шаблона.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Использование стандартных строковых шаблонов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911484"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="748d7-103">Использование стандартных строковых шаблонов</span><span class="sxs-lookup"><span data-stu-id="748d7-103">Using Standard String Templates</span></span>

<span data-ttu-id="748d7-104">Несколько потребителей, например потребитель событий активных скриптов или потребитель событий командной строки, имеют свойства строки с квалификатором **шаблона** .</span><span class="sxs-lookup"><span data-stu-id="748d7-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="748d7-105">Эти свойства используют стандартные строковые шаблоны для создания строки, которая настраивается в части экземпляром потребителя и частью события.</span><span class="sxs-lookup"><span data-stu-id="748d7-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="748d7-106">Структура стандартного строкового шаблона аналогична спецификации переменной среды Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="748d7-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="748d7-107">В следующем списке приведены некоторые примеры языка шаблона:</span><span class="sxs-lookup"><span data-stu-id="748d7-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="748d7-108">Строка "некоторый текст" всегда создает строку "некоторый текст".</span><span class="sxs-lookup"><span data-stu-id="748d7-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="748d7-109">"% График%" всегда создает значение свойства **график** для доставляемого события.</span><span class="sxs-lookup"><span data-stu-id="748d7-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="748d7-110">Если свойство не является строкой, оно преобразуется в строку. Например, "90" или "TRUE".</span><span class="sxs-lookup"><span data-stu-id="748d7-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="748d7-111">"Использование ЦП этим процессором% график% в настоящее время" внедряет значение свойства **график** события в строку, создавая нечто вроде "Загрузка ЦП этим процессором в настоящее время 90".</span><span class="sxs-lookup"><span data-stu-id="748d7-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="748d7-112">"% TargetInstance. график%" получает значение свойства **график** в внедренном экземпляре свойства **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="748d7-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="748d7-113">"%%" создает один знак%.</span><span class="sxs-lookup"><span data-stu-id="748d7-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="748d7-114">Если извлекаемое свойство является массивом, весь массив создается в следующем формате: "(1, 5, 10, 1024)".</span><span class="sxs-lookup"><span data-stu-id="748d7-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="748d7-115">Если в массиве присутствует только один элемент, скобки опускаются.</span><span class="sxs-lookup"><span data-stu-id="748d7-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="748d7-116">Если в массиве нет элементов, создается "()".</span><span class="sxs-lookup"><span data-stu-id="748d7-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="748d7-117">Если свойство является внедренным объектом, создается MOF-представление объекта (аналогично методу [**ивбемклассобжект:: жетобжекттекст**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="748d7-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="748d7-118">Если запрашивается свойство внедренного массива объектов, оно обрабатывается как свойство со значением массива.</span><span class="sxs-lookup"><span data-stu-id="748d7-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="748d7-119">Например:% Мевентс. TargetInstance. Дриверлеттер% может создать "(" C: "," D: ")", если Мевентс является массивом событий изменения внедренного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="748d7-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="748d7-120">Строковые литералы</span><span class="sxs-lookup"><span data-stu-id="748d7-120">String Literals</span></span>

<span data-ttu-id="748d7-121">Все, что находится внутри пары кавычек, считается строковым литералом и не будет заменено.</span><span class="sxs-lookup"><span data-stu-id="748d7-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="748d7-122">В следующем примере показана строка, которую компилятор видит при использовании "Загрузка ЦП% график%".</span><span class="sxs-lookup"><span data-stu-id="748d7-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="748d7-123">Эта строка возвращает следующие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="748d7-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="748d7-124">С другой стороны, строка "Загрузка ЦП \\ "% график% \\ "показана компилятором следующим образом.</span><span class="sxs-lookup"><span data-stu-id="748d7-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="748d7-125">Эта строка выдает следующие выходные данные без подстановки переменных.</span><span class="sxs-lookup"><span data-stu-id="748d7-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="748d7-126">См. также</span><span class="sxs-lookup"><span data-stu-id="748d7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748d7-127">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="748d7-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



