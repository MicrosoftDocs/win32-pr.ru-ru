---
title: Структура MCI_WAVE_SET_PARMS (МЦиапи. h)
description: '\_ \_ \_ Структура пармс набора звукозаписи MCI содержит сведения для команды MCI \_ Set для устройств аудио-Audio.'
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- структура MCI_WAVE_SET_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85508ec493ecdc38825b90877e608683fe6c0bb7c099365c187a434890c605d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783754"
---
# <a name="mci_wave_set_parms-structure"></a>\_ \_ Структура пармс набора ЗВУКОзаписи MCI \_

Структура **\_ \_ \_ Пармс набора** звукозаписи MCI содержит сведения для команды [**MCI \_ Set**](mci-set.md) для устройств аудио-Audio.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двтимеформат**
</dt> <dd>

Формат времени устройства.

</dd> <dt>

**дваудио**
</dt> <dd>

Номер канала для выходных данных звука. Обычно используется при включении или отключении канала.

</dd> <dt>

**винпут**
</dt> <dd>

Входной канал звука.

</dd> <dt>

**ваутпут**
</dt> <dd>

Используемое устройство вывода. Например, это значение может быть равно 2, если в системе имеется две установленные звуковые карты.

</dd> <dt>

**вформаттаг**
</dt> <dd>

Формат данных звуковой волны, например \_ Формат \_ PCM. Возможные значения определены в Ммрег. h.

</dd> <dt>

**wReserved2**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**нчаннелс**
</dt> <dd>

Моно (1) или стерео (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**нсамплесперсек**
</dt> <dd>

Выборок в секунду.

</dd> <dt>

**навгбитесперсек**
</dt> <dd>

Частота выборки в байтах в секунду.

</dd> <dt>

**нблоккалигн**
</dt> <dd>

Заблокируйте выравнивание данных.

</dd> <dt>

**wReserved4**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**вбитсперсампле**
</dt> <dd>

Бит на выборку.

</dd> <dt>

**wReserved5**
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_набор MCI**](mci-set.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

