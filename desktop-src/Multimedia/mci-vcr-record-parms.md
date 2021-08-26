---
title: Структура MCI_VCR_RECORD_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс записи видеомагнитофона MCI \_ содержит параметры для \_ команды записи MCI для устройств записи видеокассет.'
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- структура MCI_VCR_RECORD_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b613c2b64bae1395b3fc402816145c0ef690801b9fd6402201198f7ff28a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038234"
---
# <a name="mci_vcr_record_parms-structure"></a>\_ \_ Структура пармс записи видеомагнитофона MCI \_

Структура **\_ \_ \_ пармс записи видеомагнитофона MCI** содержит параметры для команды [**\_ записи MCI**](mci-record.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

Значение времени, которое влияет [**на \_ запись MCI**](mci-record.md) или команду [**MCI \_ Cue**](mci-cue.md) . Для **\_ записи MCI** это время начала записи. В случае с MCI, это время, когда устройство куед достигает места, указанного в **двфром**. **\_**

</dd> </dl>

## <a name="remarks"></a>Remarks

Позиции указываются в текущем формате времени.

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

[**\_Подсказка MCI**](mci-cue.md)
</dt> <dt>

[**\_запись MCI**](mci-record.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

