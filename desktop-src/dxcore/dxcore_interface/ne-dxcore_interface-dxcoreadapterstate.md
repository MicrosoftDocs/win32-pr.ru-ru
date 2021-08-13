---
title: DXCoreAdapterState
description: Определяет константы, указывающие виды состояний адаптера Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6878aaccb61fd164fcf834561fcf70f13d2609de595687b6ef6301778c87f81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367084"
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