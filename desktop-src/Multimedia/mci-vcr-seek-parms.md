---
title: Структура MCI_VCR_SEEK_PARMS (видеомагнитофон. h)
description: '\_Структура пармс в видеомагнитофоне MCI \_ \_ содержит параметры для \_ команды MCI Seek для устройств записи видеокассет.'
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- структура MCI_VCR_SEEK_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee25352925681ef548310d9e009808499ce0a36f80472e50ee2a0daa71ed8dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038204"
---
# <a name="mci_vcr_seek_parms-structure"></a>\_ \_ Структура пармс в видеомагнитофоне MCI \_

Структура **\_ \_ \_ пармс в видеомагнитофоне MCI** содержит параметры для команды [**MCI \_ Seek**](mci-seek.md) для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двто**
</dt> <dd>

Положение для поиска.

</dd> <dt>

**двмарк**
</dt> <dd>

Нумерованная метка для поиска.

</dd> <dt>

**дват**
</dt> <dd>

Время начала поиска.

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

[**\_Поиск MCI**](mci-seek.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

