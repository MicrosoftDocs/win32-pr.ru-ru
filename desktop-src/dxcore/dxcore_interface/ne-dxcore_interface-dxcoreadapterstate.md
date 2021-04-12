---
title: DXCoreAdapterState
description: Определяет константы, указывающие виды состояний адаптера Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338041"
---
# <a name="dxcoreadapterstate-enum"></a>Перечисление Дкскореадаптерстате

Определяет константы, указывающие виды состояний адаптера Дкскоре. Передайте одну из этих констант методу [идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) , чтобы получить элемент состояния адаптера для типа состояния. Передайте константу в метод [идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md) , чтобы задать сведения о адаптере для элемента состояния.

## <a name="syntax"></a>Синтаксис

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Константы

### <a name="isdriverupdateinprogress"></a>исдриверупдатеинпрогресс

Указывает состояние адаптера <em>исдриверупдатеинпрогресс</em> , которое `true` указывает, что на адаптере было инициировано обновление драйвера, но оно еще не завершено. Если обновление драйвера уже завершено, адаптер станет недействительным, и вызов [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) возвратит значение <b>HRESULT</b> <b>DXGI_ERROR_DEVICE_REMOVED</b>.

При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)элемент состояния <em>исдриверупдатеинпрогресс</em> имеет тип <b>uint8_t</b>, представляющий логическое значение.

<b>Важное</b> — Этот элемент состояния не поддерживается для [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).

### <a name="adaptermemorybudget"></a>адаптермеморибуджет

Указывает состояние адаптера <em>адаптермеморибуджет</em> , которое извлекает или запрашивает бюджет памяти адаптера на адаптере.

При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">Дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> для *outputBuffer*.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md), [Идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)