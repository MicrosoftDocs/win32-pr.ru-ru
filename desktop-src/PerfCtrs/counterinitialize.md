---
description: Регистрирует поставщик и инициализирует наборы счетчиков.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Функция Каунтеринитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998529"
---
# <a name="counterinitialize-function"></a>Функция Каунтеринитиализе

Регистрирует поставщик и инициализирует наборы счетчиков.

## <a name="syntax"></a>Синтаксис


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает ошибку \_ успешного выполнения; в противном случае — стандартный код ошибки Win32.

## <a name="remarks"></a>Комментарии

Поставщик вызывает эту функцию. Функция включает вызовы функции [**перфстартпровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) и функции [**перфсеткаунтерсетинфо**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

Средство [**КТРПП**](ctrpp.md) создает эту встроенную функцию при указании аргумента **-o** . Имя функции включает строку *префикса* , если указан аргумент **-prefix** .

Если указать аргументы **-меморираутинес** или **-нотификатионкаллбакк** (или указать атрибут **обратного вызова** для элемента [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), то сигнатура **каунтеринитиализе** изменяется следующим образом:

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

где

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>нотификатионкаллбакк
</dt> <dd>

Имя функции обратного вызова [*контролкаллбакк*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) , которая реализуется для получения уведомлений о запросах потребителей (например, запросов на добавление или удаление счетчиков из запроса). Если не реализовать функцию обратного вызова *контролкаллбакк* , задайте значение **null** .

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>меморяллокатионфунктион
</dt> <dd>

Имя функции обратного вызова [*аллокатемемори*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) , которая вызывается в PERFLIB для выделения памяти. Задайте **значение NULL** , если не был указан аргумент **-меморираутинес** .

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>меморифрифунктион
</dt> <dd>

Имя функции обратного вызова [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) , вызывающей PERFLIB для освобождения памяти, выделенной с помощью функции [*аллокатемемори*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) . Задайте **значение NULL** , если *Меморяллокатионфунктион* имеет **значение NULL**.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>меморифунктионконтекст
</dt> <dd>

Контекстные сведения, передаваемые в подпрограммы выделения памяти и свободные. Может иметь **значение NULL**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

