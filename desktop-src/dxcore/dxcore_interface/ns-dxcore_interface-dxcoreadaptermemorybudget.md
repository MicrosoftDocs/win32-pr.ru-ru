---
title: DXCoreAdapterMemoryBudget
description: Описывает бюджет памяти для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488197"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>Структура Дкскореадаптермеморибуджет

Указывает состояние адаптера <em>адаптермеморибуджет</em> , которое извлекает или запрашивает бюджет памяти адаптера на адаптере. Установка (запрос) бюджета представляет минимальный объем физической памяти, необходимый для резервирования адаптера (в байтах). Рекомендуется настроить резервирование адаптера, чтобы обозначить объем физической памяти, которую приложение не может использовать. Это значение помогает операционной системе (ОС) быстро уменьшить влияние больших случаев нехватки памяти.

При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">Дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип **DXCoreAdapterMemoryBudget** для *outputBuffer*.

При вызове [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип **uint64_t** для *inputData*.

## <a name="syntax"></a>Синтаксис

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Члены

### <a name="budget"></a>составлен

Тип: **uint64_t**

Указывает предоставляемый ОС бюджет памяти (в байтах), который должно быть целевое приложение. Если *куррентусаже* больше, чем *бюджет*, приложение может повлечь за собой "дергания" или снижения производительности из-за фоновых действий операционной системы, которая предназначена для предоставления другим приложениям достаточного использования памяти адаптера.

### <a name="currentusage"></a>куррентусаже

Тип: **uint64_t**

Указывает текущее использование памяти адаптера приложения отменено в байтах.

### <a name="availableforreservation"></a>аваилаблефорресерватион

Тип: **uint64_t**

Указывает объем памяти адаптера в байтах, доступный для резервирования приложением. Чтобы зарезервировать эту память адаптера, приложение должно вызвать [идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md) с *состоянием* , установленным в [дкскореадаптерстате:: адаптермеморибуджет](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>куррентресерватион

Тип: **uint64_t**

Указывает объем памяти адаптера в байтах, зарезервированный приложением. ОС использует резервирование в качестве подсказки для определения минимального рабочего набора приложения. Приложение должно попытаться отрезать использование памяти адаптера в соответствии с этим требованием.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)