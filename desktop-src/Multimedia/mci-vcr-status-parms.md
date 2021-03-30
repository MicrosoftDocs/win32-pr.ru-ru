---
title: Структура MCI_VCR_STATUS_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс состояния видеомагнитофона MCI \_ содержит параметры команды "состояние MCI" \_ для устройств записи видеокассет.'
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988262"
---
# <a name="mci_vcr_status_parms-structure"></a>\_ \_ Структура пармс состояния видеомагнитофона MCI \_

Структура **\_ \_ \_ пармс состояния видеомагнитофона MCI** содержит параметры команды " [**\_ состояние MCI**](mci-status.md) " для устройств записи видеокассет.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двретурн**
</dt> <dd>

Значение, возвращаемое командой " [**\_ состояние MCI**](mci-status.md) ". Возвращаемое значение зависит от запроса команды. Дополнительные сведения см. в описании команды [**\_ состояния MCI**](mci-status-parms.md) .

</dd> <dt>

**двитем**
</dt> <dd>

Тип запрашиваемой информации.

</dd> <dt>

**двтракк**
</dt> <dd>

Звуковая или видеодорожка, которая будет хранить информацию во время следующей записи. Этот элемент используется для возврата сведений, когда команда [**MCI \_ Status**](mci-status-parms.md) выдает запрос о состоянии записи видео или звука.

</dd> <dt>

**двнумбер**
</dt> <dd>

Логический тюнер, с которым связан текущий канал. Этот элемент используется для возврата сведений, когда команда [**MCI \_ Status**](mci-status.md) запрашивать сведения о текущем номере канала.

</dd> </dl>

## <a name="remarks"></a>Комментарии

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

[**\_состояние MCI**](mci-status.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

