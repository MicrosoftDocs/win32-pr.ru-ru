---
title: Распространенные ошибки компилятора
description: В этом разделе показаны типичные ошибки компилятора, возникающие при переносе существующей базы кода. Эти примеры происходят из кода HAL на уровне системы, хотя эти понятия напрямую применимы к коду уровня пользователя.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- ошибки компилятора 64-разрядное программирование для Windows
- Миграция 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339696"
---
# <a name="common-compiler-errors"></a><span data-ttu-id="6fd2b-106">Распространенные ошибки компилятора</span><span class="sxs-lookup"><span data-stu-id="6fd2b-106">Common Compiler Errors</span></span>

<span data-ttu-id="6fd2b-107">В этом разделе показаны типичные ошибки компилятора, возникающие при переносе существующей базы кода.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="6fd2b-108">Эти примеры происходят из кода HAL на уровне системы, хотя эти понятия напрямую применимы к коду уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="6fd2b-109">Предупреждение C4311. Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fd2b-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="6fd2b-110">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "Long без знака</span><span class="sxs-lookup"><span data-stu-id="6fd2b-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="6fd2b-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-113">**Птртаулонг** — это встроенная функция или макрос в зависимости от используемого использования.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="6fd2b-114">Он усекает указатель до **ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="6fd2b-115">Хотя 32-разрядные указатели не затрагиваются, верхняя половина 64-разрядного указателя усекается.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="6fd2b-116">CIA \_ \_ Конфигурация PCI \_ Базовая \_ кВА объявляется как **PVOID**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="6fd2b-117">Приведение **ulong** работает в 32-разрядном мире, но приводит к ошибке в 64-разрядном мире.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="6fd2b-118">Решением является получение 64-разрядного указателя на **ulong**, поскольку изменение определения объединения, которое ппЦиаддр->u. асулонг, определено в, изменяет слишком много кода.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="6fd2b-119">Использование макроса **птртаулонг** для преобразования 64-разрядного **PVOID** в требуемый **ulong** разрешено, так как у нас есть сведения о конкретном значении CIA \_ PCI \_ config \_ Base \_ кВА.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="6fd2b-120">В этом случае этот указатель никогда не будет содержать данные в верхнем 32 бит.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="6fd2b-122">Предупреждение C4311, пример 2</span><span class="sxs-lookup"><span data-stu-id="6fd2b-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="6fd2b-123">"приведение типа": усечение указателя из "ошибка структуры" \_ \_ кадра \* \_ \_ ptr64 "в" Long без знака</span><span class="sxs-lookup"><span data-stu-id="6fd2b-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="6fd2b-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-126">Проблема заключается в том, что последний параметр этой функции является указателем на структуру данных.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="6fd2b-127">Поскольку Пункорректаблиррор является указателем, он изменяет размер с помощью модели программирования.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="6fd2b-128">Прототип для **кебугчеккекс** был изменен так, чтобы последний параметр был типа **ulong \_**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="6fd2b-129">В результате необходимо привести указатель функции к типу записи **\_ типа ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="6fd2b-130">Вы можете спросить, почему **PVOID** не использовался в качестве последнего параметра.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="6fd2b-131">В зависимости от контекста вызова последний параметр может быть не указателем или, возможно, кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="6fd2b-133">Предупреждение C4244, пример 1</span><span class="sxs-lookup"><span data-stu-id="6fd2b-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="6fd2b-134">"=": преобразование из " \_ компонент конфигурации \_ структуры \* \_ \_ ptr64" в " \_ компонент конфигурации \_ структуры \* ", возможна утрата данных</span><span class="sxs-lookup"><span data-stu-id="6fd2b-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="6fd2b-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-137">Функция объявляет компонент переменной в качестве \_ компонента пконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="6fd2b-138">Позже переменная будет использоваться в следующем назначении, которое отображается правильно:</span><span class="sxs-lookup"><span data-stu-id="6fd2b-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="6fd2b-139">Однако компонент типа ПКОНФИГУРАТИОН \_ определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6fd2b-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="6fd2b-140">Определение типа для компонента ПКОНФИГУРАТИОН \_ предоставляет 32-разрядный указатель как в 32-разрядных, так и в 64-разрядных моделях, так как он объявлен как **указатель \_ 32**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="6fd2b-141">Исходный конструктор этой структуры знал, что он будет использоваться в 32-разрядном контексте в BIOS и явно определен для этого использования.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="6fd2b-142">Этот код прекрасно работает в 32-разрядных Windows, так как указатели должны быть 32-разрядными.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="6fd2b-143">В 64-разрядной версии Windows она не работает, поскольку код находится в 64-разрядном контексте.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-145">Чтобы обойти эту проблему, используйте компонент конфигурации, \_ \* а не 32-разрядный \_ компонент пконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="6fd2b-146">Очень важно четко понимать назначение кода.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="6fd2b-147">Если этот код предназначен для 32 сенсорного управления BIOS или системным пространством, это исправление не будет работать.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="6fd2b-148">**Указатель \_ 32** определен в нтдеф. h и Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="6fd2b-149">Предупреждение C4242, пример 2</span><span class="sxs-lookup"><span data-stu-id="6fd2b-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="6fd2b-150">"=": преобразование " \_ \_ Int64" в "без знака Long", возможна утрата данных</span><span class="sxs-lookup"><span data-stu-id="6fd2b-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span data-ttu-id="6fd2b-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-153">Это предупреждение создается потому, что вычисление использует 64-битные значения, в данном случае указатели и помещает результат в 32-разрядный **ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-155">Приведите результат вычисления к типу **ulong** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="6fd2b-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="6fd2b-156">Приведение результата позволяет компилятору узнать, что вы уверены в результатах.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="6fd2b-157">С другой стороны, убедитесь, что вы понимаете вычисление и уверены, что оно поместится в 32-разрядном **ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="6fd2b-158">Если результат может не уместиться в 32-разрядном **ulong**, измените базовый тип переменной, которая будет содержать результат.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="6fd2b-159">Предупреждение C4311-пример 1</span><span class="sxs-lookup"><span data-stu-id="6fd2b-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="6fd2b-160">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="6fd2b-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span data-ttu-id="6fd2b-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-163">Эта функция работает с адресами в виде целых чисел, что требует обязательного ввода этих целых чисел в переносимом виде.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="6fd2b-164">Все локальные переменные, промежуточные значения в вычислениях и возвращаемые значения должны быть переносимыми типами.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

<span data-ttu-id="6fd2b-166">**Пулонг \_ PTR** — это указатель, который сам по себе является 32 бит для 32-разрядной версии Windows и 64 бит для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="6fd2b-167">Он указывает на целое число без знака **\_ типа ulong**, которое 32 бит для 32-разрядной версии Windows и 64 бит для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="6fd2b-168">Предупреждение C4311-пример 2</span><span class="sxs-lookup"><span data-stu-id="6fd2b-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="6fd2b-169">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="6fd2b-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span data-ttu-id="6fd2b-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-172">Несмотря на то, что все значения кВА (с небольшими виртуальными адресами) действительно являются 32-разрядными на этом этапе и будут помещаться в **ulong**, более единообразно обрабатывать все адреса как значения **\_ типа ulong** , если это возможно.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="6fd2b-173">Указатель ПЦииоспацебасе содержит кВА, созданный в макросе HAL, \_ \_ кВА.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="6fd2b-174">Этот макрос возвращает 64-разрядное значение с максимальным значением 32, равное нулю, поэтому математические вычисления будут работать.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="6fd2b-175">Можно просто оставить код для усечения указателя в **ulong**, но такой подход не рекомендуется для повышения удобства поддержки и переносимости кода.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="6fd2b-176">Например, содержимое кВА может измениться в будущем, чтобы использовать некоторые верхние биты на этом уровне, нарушая код.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-178">Будьте в безопасности и используйте **ulong \_ ptr** для всех математических адресов и указателей.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="6fd2b-179">Предупреждение C4311. Пример 3</span><span class="sxs-lookup"><span data-stu-id="6fd2b-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="6fd2b-180">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="6fd2b-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span data-ttu-id="6fd2b-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-183">Компилятор предупреждает о адресе (&) и операторах сдвига влево (<<), если они применяются к типам указателей.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="6fd2b-184">В приведенном выше коде кВА является значением **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="6fd2b-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="6fd2b-185">Для выполнения математических операций необходимо привести его к целому типу.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="6fd2b-186">Поскольку код должен быть переносимым, используйте **ulong \_ ptr** вместо **ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="6fd2b-188">Предупреждение C4311. Пример 4</span><span class="sxs-lookup"><span data-stu-id="6fd2b-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="6fd2b-189">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="6fd2b-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="6fd2b-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-192">Транслатедаддресс — это объединение, которое выглядит примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6fd2b-192">TranslatedAddress is a union that looks something like the following:</span></span>

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span data-ttu-id="6fd2b-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-194">Зная, что остальная часть кода может поместиться в Хигхпарт, мы можем выбрать любое из приведенных здесь решений.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="6fd2b-195">Макрос **птртаулонг** усекает указатель, возвращенный **халкреатеква** , в 32 бит.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="6fd2b-196">Мы понимаем, что кВА, возвращенный **халкреатеква** , имеет нулевые 32 верхние биты, равные нулю, а самая Следующая строка кода настраивает транслатедаддресс->хигхпарт в ноль.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="6fd2b-197">С осторожностью мы могли бы использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="6fd2b-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="6fd2b-198">Это работает в этом примере: макрос **халкреатеква** возвращает 64 бит, а верхние 32-биты имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="6fd2b-199">Просто будьте внимательны, чтобы не оставлять верхние 32 бит, не применяя в 32-разрядной среде, которая может фактически выполняться в этом втором решении.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="6fd2b-200">Предупреждение C4311. Пример 5</span><span class="sxs-lookup"><span data-stu-id="6fd2b-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="6fd2b-201">"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="6fd2b-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="6fd2b-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="6fd2b-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span data-ttu-id="6fd2b-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="6fd2b-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6fd2b-204">Виндоврегистерс->Виндовбасе является указателем и теперь имеет 64 бит.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="6fd2b-205">В коде написано, что это значение равно 20 битам сдвига вправо.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="6fd2b-206">Компилятор не позволяет использовать оператор сдвига вправо (>>) для указателя; Поэтому необходимо привести его к целому числу.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="6fd2b-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение</span><span class="sxs-lookup"><span data-stu-id="6fd2b-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="6fd2b-208">Приведение к типу **ulong- \_ ptr** — это именно то, что нам нужно.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="6fd2b-209">Следующая проблема — Вбасе.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-209">The next problem is Wbase.</span></span> <span data-ttu-id="6fd2b-210">Вбасе — это **ulong** , а — 32 бит.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="6fd2b-211">В этом случае мы понимаем, что 64-разрядный указатель Виндоврегистерс->Виндовбасе является допустимым в младших 32 битах даже после сдвига.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="6fd2b-212">Это делает использование макроса **птртаулонг** приемлемым, так как он усекает 64-разрядный указатель в 32-разрядный **ulong**.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="6fd2b-213">Приведение **PVOID** необходимо, так как **птртаулонг** требует аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="6fd2b-214">Когда вы взгляните на полученный код ассемблера, все это приведение кода на языке C превращается в небольшую, правую, сдвиг вправо и хранение длиннее.</span><span class="sxs-lookup"><span data-stu-id="6fd2b-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




