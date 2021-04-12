---
description: Вы пытаетесь найти дополнительные сведения об объектах Direct3D во время отладки? Например, на следующем снимке экрана показано, что обычно отображается при просмотре интерфейса Direct3D в окне Контрольные значения.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Включение отладочной информации Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139222"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="20401-104">Включение отладочной информации Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="20401-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="20401-105">Вы пытаетесь найти дополнительные сведения об объектах Direct3D во время отладки?</span><span class="sxs-lookup"><span data-stu-id="20401-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="20401-106">Например, на следующем снимке экрана показано, что обычно отображается при просмотре интерфейса Direct3D в окне Контрольные значения.</span><span class="sxs-lookup"><span data-stu-id="20401-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![снимок экрана интерфейса Direct3D в окне "контрольные значения"](images/d3d-debug-info1.png)

<span data-ttu-id="20401-108">Можно включить основные объекты отладки, чтобы в окне Контрольные значения можно было просматривать зеркальный объект, содержащий все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="20401-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="20401-109">Просто включите следующее \# Определение в код перед ФАЙЛОМ d3d9. h:</span><span class="sxs-lookup"><span data-stu-id="20401-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="20401-110">Чтобы включить отладочную информацию, \# Определение должно быть создано перед ФАЙЛОМ d3d9. h (любая программа, использующая дксут, автоматически включит \_ отладочные \_ данные D3D при компиляции программы для отладки).</span><span class="sxs-lookup"><span data-stu-id="20401-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="20401-111">Если вы используете пример пакета SDK, это можно увидеть в Дксстдафкс. h (который влияет на все примеры C++).</span><span class="sxs-lookup"><span data-stu-id="20401-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="20401-112">Также необходимо запустить отладочную среду выполнения Direct3D (при необходимости ее можно включить на панели управления).</span><span class="sxs-lookup"><span data-stu-id="20401-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="20401-113">Ниже приведен пример использования [примера басичлсл](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="20401-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="20401-114">Добавьте \# Определение в файл дксстдафкс. h перед строкой 37.</span><span class="sxs-lookup"><span data-stu-id="20401-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="20401-115">Создайте проект отладки.</span><span class="sxs-lookup"><span data-stu-id="20401-115">Build a debug project.</span></span>
3.  <span data-ttu-id="20401-116">Установка точки останова в строке 307 в Басичлсл. cpp</span><span class="sxs-lookup"><span data-stu-id="20401-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="20401-117">Запустите отладчик.</span><span class="sxs-lookup"><span data-stu-id="20401-117">Run the debugger.</span></span>

<span data-ttu-id="20401-118">На следующем снимке экрана показан тип подробных сведений, которые можно получить о объекте текстуры Direct3D из окна Контрольные значения.</span><span class="sxs-lookup"><span data-stu-id="20401-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![снимок экрана объекта текстуры Direct3D в окне "контрольные значения"](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="20401-120">Имена свойств объектов видимы, а значения верны только при включенной среде выполнения отладки.</span><span class="sxs-lookup"><span data-stu-id="20401-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="20401-121">При запуске в среде выполнения розничной торговли значения недопустимы.</span><span class="sxs-lookup"><span data-stu-id="20401-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="20401-122">Использование стека вызовов для расширенной отладки</span><span class="sxs-lookup"><span data-stu-id="20401-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="20401-123">При включенной отладке Direct3D можно также просматривать стек вызовов каждый раз при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="20401-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="20401-124">Это сделает ваше приложение очень ресурсоемким, но его можно использовать для проверки утечек ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20401-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="20401-125">Чтобы записать стек вызовов, задайте для следующего раздела реестра значение 1:</span><span class="sxs-lookup"><span data-stu-id="20401-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="20401-126">Сборка приложения с включенной отладкой предоставит вам доступ к этой дополнительной переменной:</span><span class="sxs-lookup"><span data-stu-id="20401-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="20401-127">Эта переменная будет хранить стек вызовов каждый раз при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="20401-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="20401-128">Это сделает ваше приложение очень ресурсоемким, но может использоваться для отладки утечек ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20401-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20401-129">См. также</span><span class="sxs-lookup"><span data-stu-id="20401-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20401-130">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="20401-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



