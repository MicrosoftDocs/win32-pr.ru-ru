---
title: Структура _WAVEFORMATEX
description: Структура \_WAVEFORMATEX определяет формат данных, содержащих форму звуковой волны.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586749"
---
# <a name="_waveformatex-structure"></a>\_Структура ВАВЕФОРМАТЕКС

Структура **\_ вавеформатекс** определяет формат данных звуковой волны.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Члены

<dl> <dt>

**вформаттаг**
</dt> <dd>

Необходимо задать формат или форматы, поддерживаемые устройством. обратите внимание, что в предыдущих версиях Windows Media диспетчер устройств рекомендуется \_ использовать \_ формат вмдм WAVE \_ ALL для указания поддержки всех форматов. Однако это не рекомендуется, так как разные проигрыватели мультимедиа будут интерпретировать это по-разному, и несколько устройств могут реально воспроизводить любой формат файла. Теперь рекомендуется использовать \_ Допустимые значения свойства enum вмдм, \_ \_ \_ \_ любое значение перечисления [**\_ \_ \_ допустимых \_ \_ значений вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md) , или, однако, лучше указать диапазон форматов с помощью структуры [**\_ \_ \_ диапазона значений свойств вмдм**](wmdm-prop-values-range.md) .

</dd> <dt>

**нчаннелс**
</dt> <dd>

Число каналов в данных аудио-сигнала. Данные монаурал используют один канал, а стерео — два канала.

</dd> <dt>

**нсамплесперсек**
</dt> <dd>

Частота выборки, в примерах в секунду (герц), в которой каждый канал должен воспроизводиться или записываться. Распространенные значения для **нсамплесперсек** : 8,0 Килохертз (кГц), 11,025 кгц, 22,05 кгц и 44,1 кГц.

</dd> <dt>

**навгбитесперсек**
</dt> <dd>

Требуемая средняя скорость передачи данных для тега формата (в байтах в секунду). Программное обеспечение для воспроизведения и записи может оценивать размеры буфера с помощью элемента **навгбитесперсек** .

</dd> <dt>

**нблоккалигн**
</dt> <dd>

Выравнивание блокировки в байтах. Выравнивание блока — это минимальная атомарная единица данных для типа формата **вформаттаг** . Программное обеспечение для воспроизведения и записи должно обрабатывать несколько **нблоккалигн** байт данных за раз. Данные, записываемые и прочитанные с устройства, всегда должны начинаться в начале блока. Например, невозможно правильно начать воспроизведение данных PCM в середине примера (то есть на границе, которая не является согласованной).

</dd> <dt>

**вбитсперсампле**
</dt> <dd>

Бит на выборку для типа формата **вформаттаг** .

</dd> <dt>

**кбсизе**
</dt> <dd>

Этот элемент не учитывается.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имдспдевице:: Жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**Имдспстораже:: Креатестораже**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**Имдспстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**Ивмдмдевице:: Жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**Ивмдмоператион:: Жетобжектаттрибутес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**Ивмдмоператион:: Сетобжектаттрибутес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**Ивмдмстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





