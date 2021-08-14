---
title: Структура MCI_VCR_SETAUDIO_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТАУДИО видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сетаудио для устройств записи видеокассет.'
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- структура MCI_VCR_SETAUDIO_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa07d4cf8b88eb246019bf18dd1c1328413718a70b17ebb16e27606958473f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802962"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>\_Структура пармс видеомагнитофона MCI \_ сетаудио \_

Структура **\_ \_ \_ пармс сетаудио видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сетаудио**](mci-setaudio.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двтракк**
</dt> <dd>

Звуковая дорожка.

</dd> <dt>

**двто**
</dt> <dd>

Тип входных данных или наблюдаемых входных данных.

</dd> <dt>

**двнумбер**
</dt> <dd>

Использование звукового ввода (типа, указанного в элементе **двто** ) для использования.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Requirements (Требования)



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

[**\_СЕТАУДИО MCI**](mci-setaudio.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

