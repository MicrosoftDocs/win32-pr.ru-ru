---
title: Структура MCI_VCR_SETTUNER_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТТУНЕР видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сеттунер для устройств записи видеокассет.'
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- структура MCI_VCR_SETTUNER_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6d297ae86ad50ee9c7bb19a1f98ef69c77d502f4ccd306394436d07de330d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784176"
---
# <a name="mci_vcr_settuner_parms-structure"></a>\_Структура пармс видеомагнитофона MCI \_ сеттунер \_

Структура **\_ \_ \_ пармс сеттунер видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сеттунер**](mci-settuner.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двчаннел**
</dt> <dd>

Номер нового канала.

</dd> <dt>

**двнумбер**
</dt> <dd>

Логический тюнер, на который влияет команда [**MCI \_ сеттунер**](mci-settuner.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

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

[**\_СЕТТУНЕР MCI**](mci-settuner.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

