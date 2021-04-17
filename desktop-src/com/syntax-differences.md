---
title: Синтаксические отличия
description: Самым очевидным изменением при переходе между языками программирования является изменение синтаксиса.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488337"
---
# <a name="syntax-differences"></a><span data-ttu-id="db802-103">Синтаксические отличия</span><span class="sxs-lookup"><span data-stu-id="db802-103">Syntax Differences</span></span>

<span data-ttu-id="db802-104">Самым очевидным изменением при переходе между языками программирования является изменение синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="db802-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="db802-105">Рассмотрим метод Add объекта Енхевентс, показанный в том виде, в котором он объявлен на трех разных языках.</span><span class="sxs-lookup"><span data-stu-id="db802-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

<span data-ttu-id="db802-106">Хотя синтаксис каждого языка выражает метод по-разному, функциональные возможности одинаковы.</span><span class="sxs-lookup"><span data-stu-id="db802-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="db802-107">В каждом языке метод Add принимает параметры *time* и *Name* и возвращает объект енхевент.</span><span class="sxs-lookup"><span data-stu-id="db802-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="db802-108">В примере C++ метод возвращает объект, используя третий, выходной параметр *Pval*.</span><span class="sxs-lookup"><span data-stu-id="db802-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="db802-109">Как правило, функциональные возможности COM-объекта одинаковы в разных языках программирования.</span><span class="sxs-lookup"><span data-stu-id="db802-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="db802-110">По этой причине документация для COM-объекта полезна даже в том случае, если объект документирован на другом языке программирования, отличном от того, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="db802-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="db802-111">Описания функциональности объекта, параметров и возвращаемых значений — это, за некоторыми исключениями, допустимыми для всех языков.</span><span class="sxs-lookup"><span data-stu-id="db802-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="db802-112">Сведения о преобразовании синтаксиса COM-объекта на другой язык программирования см. в разделе [преобразование синтаксиса COM-объекта для языков программирования](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="db802-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="db802-113">Различия синтаксиса в языках сценариев JavaScript, JScript и VBScript менее заметны, чем различия в синтаксисе между языками программирования, показанными выше.</span><span class="sxs-lookup"><span data-stu-id="db802-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="db802-114">Например, рассмотрим функцию Square, так как она реализована на каждом из трех языков сценариев:</span><span class="sxs-lookup"><span data-stu-id="db802-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="db802-115">Обратите внимание, что языки сценариев, в отличие от языков программирования, слабо типизированы.</span><span class="sxs-lookup"><span data-stu-id="db802-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="db802-116">Иными словами, не нужно указывать тип данных параметра или возвращаемого значения при объявлении функции.</span><span class="sxs-lookup"><span data-stu-id="db802-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="db802-117">Вместо этого переменные автоматически приводятся к соответствующему типу данных.</span><span class="sxs-lookup"><span data-stu-id="db802-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="db802-118">В случае VBScript все переменные имеют один и тот же тип данных **Variant**.</span><span class="sxs-lookup"><span data-stu-id="db802-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="db802-119">Синтаксис JavaScript и JScript для Square одинаков.</span><span class="sxs-lookup"><span data-stu-id="db802-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="db802-120">JScript в значительной степени совместим с JavaScript.</span><span class="sxs-lookup"><span data-stu-id="db802-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="db802-121">Однако в JScript есть некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как **активексобжект**, **Enumerator**, **Error**, **Global** и **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="db802-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="db802-122">Дополнительные сведения об этих объектах см. в [справочнике по языку JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="db802-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="db802-123">На поверхности синтаксис JavaScript и JScript напоминает синтаксис Java.</span><span class="sxs-lookup"><span data-stu-id="db802-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="db802-124">Такое сходство является только недостаточной.</span><span class="sxs-lookup"><span data-stu-id="db802-124">This similarity is only superficial.</span></span> <span data-ttu-id="db802-125">Язык Java был разработан независимо от JavaScript и JScript и не связан ни с одним из них.</span><span class="sxs-lookup"><span data-stu-id="db802-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="db802-126">С другой стороны, VBScript — это подмножество языка программирования Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="db802-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="db802-127">По этой причине синтаксис VBScript является подмножеством синтаксиса Visual Basic и часто является взаимозаменяемым с синтаксисом Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="db802-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="db802-128">Сведения об использовании COM-объектов в языках сценариев см. в разделе [Создание скриптов с помощью COM-объектов](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="db802-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 