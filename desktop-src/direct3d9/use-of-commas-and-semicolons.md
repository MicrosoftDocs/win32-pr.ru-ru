---
description: Использование запятых и точек с запятой может быть наиболее сложной проблемой синтаксиса в формате файла, и это использование очень строго. Запятые используются для разделения элементов массива; точка с запятой завершает каждый элемент данных.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Использование запятых и точек с запятой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140699"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="1b9cd-104">Использование запятых и точек с запятой</span><span class="sxs-lookup"><span data-stu-id="1b9cd-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="1b9cd-105">Использование запятых и точек с запятой может быть наиболее сложной проблемой синтаксиса в формате файла, и это использование очень строго.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="1b9cd-106">Запятые используются для разделения элементов массива; точка с запятой завершает каждый элемент данных.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="1b9cd-107">Например, если шаблон определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b9cd-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="1b9cd-108">Затем экземпляр этого шаблона выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b9cd-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="1b9cd-109">Если шаблон, содержащий другой шаблон, определен следующим образом;</span><span class="sxs-lookup"><span data-stu-id="1b9cd-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="1b9cd-110">Затем экземпляр этого шаблона выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b9cd-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="1b9cd-111">Обратите внимание, что вторая строка, представляющая митемп внутри контейнера, содержит две точки с запятой в конце строки.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="1b9cd-112">Первая точка с запятой обозначает конец элемента данных, Атемп (внутри контейнера), а вторая точка с запятой обозначает конец контейнера.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="1b9cd-113">Если массив определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b9cd-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="1b9cd-114">Затем экземпляр этого типа выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b9cd-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="1b9cd-115">В примере массива не требуется, чтобы элементы данных были разделены точкой с запятой, так как они разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="1b9cd-116">Точка с запятой в конце отмечает конец массива.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="1b9cd-117">Рассмотрим шаблон, содержащий массив элементов данных, определенных шаблоном.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="1b9cd-118">Экземпляр этого типа будет выглядеть, как в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1b9cd-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="1b9cd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1b9cd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9cd-120">Кодировка текста</span><span class="sxs-lookup"><span data-stu-id="1b9cd-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



