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
# <a name="common-compiler-errors"></a>Распространенные ошибки компилятора

В этом разделе показаны типичные ошибки компилятора, возникающие при переносе существующей базы кода. Эти примеры происходят из кода HAL на уровне системы, хотя эти понятия напрямую применимы к коду уровня пользователя.

## <a name="warning-c4311-example-1"></a>Предупреждение C4311. Пример 1

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "Long без знака

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

**Птртаулонг** — это встроенная функция или макрос в зависимости от используемого использования. Он усекает указатель до **ulong**. Хотя 32-разрядные указатели не затрагиваются, верхняя половина 64-разрядного указателя усекается.

CIA \_ \_ Конфигурация PCI \_ Базовая \_ кВА объявляется как **PVOID**. Приведение **ulong** работает в 32-разрядном мире, но приводит к ошибке в 64-разрядном мире. Решением является получение 64-разрядного указателя на **ulong**, поскольку изменение определения объединения, которое ппЦиаддр->u. асулонг, определено в, изменяет слишком много кода.

Использование макроса **птртаулонг** для преобразования 64-разрядного **PVOID** в требуемый **ulong** разрешено, так как у нас есть сведения о конкретном значении CIA \_ PCI \_ config \_ Base \_ кВА. В этом случае этот указатель никогда не будет содержать данные в верхнем 32 бит.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Предупреждение C4311, пример 2

"приведение типа": усечение указателя из "ошибка структуры" \_ \_ кадра \* \_ \_ ptr64 "в" Long без знака

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Проблема заключается в том, что последний параметр этой функции является указателем на структуру данных. Поскольку Пункорректаблиррор является указателем, он изменяет размер с помощью модели программирования. Прототип для **кебугчеккекс** был изменен так, чтобы последний параметр был типа **ulong \_**. В результате необходимо привести указатель функции к типу записи **\_ типа ulong**.

Вы можете спросить, почему **PVOID** не использовался в качестве последнего параметра. В зависимости от контекста вызова последний параметр может быть не указателем или, возможно, кодом ошибки.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Предупреждение C4244, пример 1

"=": преобразование из " \_ компонент конфигурации \_ структуры \* \_ \_ ptr64" в " \_ компонент конфигурации \_ структуры \* ", возможна утрата данных

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Функция объявляет компонент переменной в качестве \_ компонента пконфигуратион. Позже переменная будет использоваться в следующем назначении, которое отображается правильно:

`Component = &CurrentEntry->ComponentEntry;`

Однако компонент типа ПКОНФИГУРАТИОН \_ определяется следующим образом:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

Определение типа для компонента ПКОНФИГУРАТИОН \_ предоставляет 32-разрядный указатель как в 32-разрядных, так и в 64-разрядных моделях, так как он объявлен как **указатель \_ 32**. Исходный конструктор этой структуры знал, что он будет использоваться в 32-разрядном контексте в BIOS и явно определен для этого использования. Этот код прекрасно работает в 32-разрядных Windows, так как указатели должны быть 32-разрядными. В 64-разрядной версии Windows она не работает, поскольку код находится в 64-разрядном контексте.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

Чтобы обойти эту проблему, используйте компонент конфигурации, \_ \* а не 32-разрядный \_ компонент пконфигуратион. Очень важно четко понимать назначение кода. Если этот код предназначен для 32 сенсорного управления BIOS или системным пространством, это исправление не будет работать.

**Указатель \_ 32** определен в нтдеф. h и Winnt. h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Предупреждение C4242, пример 2

"=": преобразование " \_ \_ Int64" в "без знака Long", возможна утрата данных

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Это предупреждение создается потому, что вычисление использует 64-битные значения, в данном случае указатели и помещает результат в 32-разрядный **ulong**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

Приведите результат вычисления к типу **ulong** , как показано ниже:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Приведение результата позволяет компилятору узнать, что вы уверены в результатах. С другой стороны, убедитесь, что вы понимаете вычисление и уверены, что оно поместится в 32-разрядном **ulong**.

Если результат может не уместиться в 32-разрядном **ulong**, измените базовый тип переменной, которая будет содержать результат.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Предупреждение C4311-пример 1

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Эта функция работает с адресами в виде целых чисел, что требует обязательного ввода этих целых чисел в переносимом виде. Все локальные переменные, промежуточные значения в вычислениях и возвращаемые значения должны быть переносимыми типами.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
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

**Пулонг \_ PTR** — это указатель, который сам по себе является 32 бит для 32-разрядной версии Windows и 64 бит для 64-разрядной версии Windows. Он указывает на целое число без знака **\_ типа ulong**, которое 32 бит для 32-разрядной версии Windows и 64 бит для 64-разрядной версии Windows.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Предупреждение C4311-пример 2

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Несмотря на то, что все значения кВА (с небольшими виртуальными адресами) действительно являются 32-разрядными на этом этапе и будут помещаться в **ulong**, более единообразно обрабатывать все адреса как значения **\_ типа ulong** , если это возможно.

Указатель ПЦииоспацебасе содержит кВА, созданный в макросе HAL, \_ \_ кВА. Этот макрос возвращает 64-разрядное значение с максимальным значением 32, равное нулю, поэтому математические вычисления будут работать. Можно просто оставить код для усечения указателя в **ulong**, но такой подход не рекомендуется для повышения удобства поддержки и переносимости кода. Например, содержимое кВА может измениться в будущем, чтобы использовать некоторые верхние биты на этом уровне, нарушая код.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

Будьте в безопасности и используйте **ulong \_ ptr** для всех математических адресов и указателей.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Предупреждение C4311. Пример 3

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Компилятор предупреждает о адресе (&) и операторах сдвига влево (<<), если они применяются к типам указателей. В приведенном выше коде кВА является значением **PVOID** . Для выполнения математических операций необходимо привести его к целому типу. Поскольку код должен быть переносимым, используйте **ulong \_ ptr** вместо **ulong**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Предупреждение C4311. Пример 4

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Транслатедаддресс — это объединение, которое выглядит примерно следующим образом:

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

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

Зная, что остальная часть кода может поместиться в Хигхпарт, мы можем выбрать любое из приведенных здесь решений.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

Макрос **птртаулонг** усекает указатель, возвращенный **халкреатеква** , в 32 бит. Мы понимаем, что кВА, возвращенный **халкреатеква** , имеет нулевые 32 верхние биты, равные нулю, а самая Следующая строка кода настраивает транслатедаддресс->хигхпарт в ноль.

С осторожностью мы могли бы использовать следующее:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Это работает в этом примере: макрос **халкреатеква** возвращает 64 бит, а верхние 32-биты имеют нулевое значение. Просто будьте внимательны, чтобы не оставлять верхние 32 бит, не применяя в 32-разрядной среде, которая может фактически выполняться в этом втором решении.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Предупреждение C4311. Пример 5

"приведение типа": усечение указателя из "void \* \_ \_ ptr64" в "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Виндоврегистерс->Виндовбасе является указателем и теперь имеет 64 бит. В коде написано, что это значение равно 20 битам сдвига вправо. Компилятор не позволяет использовать оператор сдвига вправо (>>) для указателя; Поэтому необходимо привести его к целому числу.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Решение
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Приведение к типу **ulong- \_ ptr** — это именно то, что нам нужно. Следующая проблема — Вбасе. Вбасе — это **ulong** , а — 32 бит. В этом случае мы понимаем, что 64-разрядный указатель Виндоврегистерс->Виндовбасе является допустимым в младших 32 битах даже после сдвига. Это делает использование макроса **птртаулонг** приемлемым, так как он усекает 64-разрядный указатель в 32-разрядный **ulong**. Приведение **PVOID** необходимо, так как **птртаулонг** требует аргумент указателя. Когда вы взгляните на полученный код ассемблера, все это приведение кода на языке C превращается в небольшую, правую, сдвиг вправо и хранение длиннее.

</dd> </dl>

 

 




