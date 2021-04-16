---
title: Структура MCI_VD_STEP_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс VD шага MCI \_ содержит сведения о \_ команде шага MCI для устройств видеодиск.'
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534199"
---
# <a name="mci_vd_step_parms-structure"></a>\_ \_ Структура пармс VD для шага MCI \_

Структура **\_ пармс VD \_ шага \_ MCI** содержит сведения о команде [**\_ шага MCI**](mci-step.md) для устройств видеодиск.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двфрамес**
</dt> <dd>

Число кадров для шага.

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

[**\_шаг MCI**](mci-step.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

