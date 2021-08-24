---
title: Структура MCI_SEQ_SET_PARMS (МЦиапи. h)
description: Структура MCI \_ Seq \_ Set \_ пармс содержит сведения о \_ команде MCI Set для устройств MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- структура MCI_SEQ_SET_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffb96cfd2f652bf989673bad68c95c6765034d2105fa554efee057faf099a9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374972"
---
# <a name="mci_seq_set_parms-structure"></a>\_Структура MCI Seq \_ Set \_ пармс

Структура **MCI \_ Seq \_ Set \_ пармс** содержит сведения о команде [**MCI \_ Set**](mci-set.md) для устройств MIDI Sequencer.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двтимеформат**
</dt> <dd>

Формат времени программы Sequencer.

</dd> <dt>

**дваудио**
</dt> <dd>

Канал вывода звука.

</dd> <dt>

**двтемпо**
</dt> <dd>

Темп.

</dd> <dt>

**двпорт**
</dt> <dd>

порт;

</dd> <dt>

**двславе**
</dt> <dd>

Тип синхронизации, используемый секвенсором для подчиненной операции.

</dd> <dt>

**двмастер**
</dt> <dd>

Тип синхронизации, используемый программой Sequencer для главной операции.

</dd> <dt>

**двоффсет**
</dt> <dd>

Смещение данных.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_набор MCI**](mci-set.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

