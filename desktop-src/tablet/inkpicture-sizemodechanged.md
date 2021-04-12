---
description: Происходит после изменения свойства Сиземоде элемента управления InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Событие InkPicture. Сиземодечанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348655"
---
# <a name="inkpicturesizemodechanged-event"></a>Событие InkPicture. Сиземодечанжед

Происходит после изменения свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) элемента управления [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Использованием NewMode* \[ окне\]
</dt> <dd>

Новое состояние элемента управления [InkPicture](inkpicture-control-reference.md) на основе нового значения свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> <dt>

*Олдмоде* \[ окне\]
</dt> <dd>

Старое состояние элемента управления [InkPicture](inkpicture-control-reference.md) , основанное на старом значении свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесиземодечанжед.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

