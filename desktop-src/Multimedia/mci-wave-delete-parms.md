---
title: Структура MCI_WAVE_DELETE_PARMS (МЦиапи. h)
description: Структура пармс "Wave" в MCI \_ \_ \_ содержит сведения о положении для \_ команды MCI DELETE для устройств аудио-аудио.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- структура MCI_WAVE_DELETE_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11633a1b6b3876f0382669856cf5971767be325906b270c4d42417e8d3f9b51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783836"
---
# <a name="mci_wave_delete_parms-structure"></a>\_ \_ Структура пармс удаления волны MCI \_

Структура **\_ \_ \_ пармс "Wave** " в MCI содержит сведения о положении для команды [**MCI \_ Delete**](mci-delete.md) для устройств аудио-аудио.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двфром**
</dt> <dd>

Расположение для удаления.

</dd> <dt>

**двто**
</dt> <dd>

Расположение для удаления.

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

[**\_Удаление MCI**](mci-delete.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

