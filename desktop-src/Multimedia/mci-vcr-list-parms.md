---
title: Структура MCI_VCR_LIST_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс в списке видеомагнитофона видеомагнитофон \_ содержит параметры для команды MCI \_ List для устройств записи видеокассет.'
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- структура MCI_VCR_LIST_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb74aeee254ab050d394dbf250c037d00d10d51fe872052dd5d36164b2c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137985"
---
# <a name="mci_vcr_list_parms-structure"></a>\_ \_ Структура пармс для списка видеомагнитофона MCI \_

Структура **\_ пармс в \_ списке \_ видеомагнитофона видеомагнитофон** содержит параметры для команды [**MCI \_ List**](mci-list.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двретурн**
</dt> <dd>

Буфер для возвращаемых данных.

</dd> <dt>

**двнумбер**
</dt> <dd>

Число видео или звуковых входов ВИДЕОМАГНИТОФОНА.

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

[**\_список MCI**](mci-list.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

