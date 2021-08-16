---
title: Структура MCI_VCR_PLAY_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс ВИДЕОМАГНИТОФОНА воспроизведения MCI \_ содержит параметры для \_ команды MCI Play для устройств записи видеокассет.'
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- структура MCI_VCR_PLAY_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2e725ca3dc04fa13dd89aff0a5fbd60ede66f83154740803c98679eb77aec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374367"
---
# <a name="mci_vcr_play_parms-structure"></a>Видеомагнитофон MCI \_ \_ воспроизводит \_ структуру пармс

Структура **\_ пармс видеомагнитофона \_ воспроизведения \_ MCI** содержит параметры для команды [**MCI \_ Play**](mci-play.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двфром**
</dt> <dd>

Расположение для воспроизведения.

</dd> <dt>

**двто**
</dt> <dd>

Расположение для воспроизведения.

</dd> <dt>

**дват**
</dt> <dd>

Значение времени, влияющее на команду [**MCI \_ Play**](mci-play.md) или командную [**\_ очередь MCI**](mci-cue.md) . Для [**\_ воспроизведения MCI**](mci-play-parms.md)это время начала воспроизведения. В случае с MCI, это время, когда устройство куед достигает места, указанного в **двфром**. **\_**

</dd> </dl>

## <a name="remarks"></a>Remarks

Позиции указываются в текущем формате времени.

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Видеомагнитофон. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_Подсказка MCI**](mci-cue.md)
</dt> <dt>

[**\_Воспроизведение MCI**](mci-play.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

