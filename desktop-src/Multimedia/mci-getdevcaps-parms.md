---
title: Структура MCI_GETDEVCAPS_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI жетдевкапс содержит сведения о устройства для команды MCI \_ жетдевкапс.'
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- MCI_GETDEVCAPS_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071317"
---
# <a name="mci_getdevcaps_parms-structure"></a>\_ \_ Структура пармс MCI жетдевкапс

Структура **\_ \_ пармс MCI жетдевкапс** содержит сведения о устройства для команды [**MCI \_ жетдевкапс**](mci-getdevcaps.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двретурн**
</dt> <dd>

Содержит сведения о выходе.

</dd> <dt>

**двитем**
</dt> <dd>

Запрашиваемая возможность. Этот элемент может быть одной из констант, перечисленных в справочном материале для команды [**MCI \_ жетдевкапс**](mci-getdevcaps.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

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

[**\_ЖЕТДЕВКАПС MCI**](mci-getdevcaps.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

