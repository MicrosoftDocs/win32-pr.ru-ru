---
title: Структура MCI_VCR_SETVIDEO_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТВИДЕО видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сетвидео для устройств записи видеокассет.'
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- структура MCI_VCR_SETVIDEO_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf260804a6e993ba133ca450a51802a0f43db3aa3d0e557ba684b8a86bcfb7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784134"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>\_Структура пармс видеомагнитофона MCI \_ сетвидео \_

Структура **\_ \_ \_ пармс сетвидео видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сетвидео**](mci-setvideo.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двтракк**
</dt> <dd>

Затронутая запись.

</dd> <dt>

**двто**
</dt> <dd>

Тип входных данных или наблюдаемых входных данных.

</dd> <dt>

**двнумбер**
</dt> <dd>

Входные данные видео (для типа, указанного в элементе **двто** ) для использования.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Видеомагнитофон. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_СЕТВИДЕО MCI**](mci-setvideo.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

