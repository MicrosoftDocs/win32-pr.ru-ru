---
description: Происходит после изменения свойства Сиземоде элемента управления InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Событие InkPicture. Сиземодечанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebcd5a659894c6f70a87ea75f7a99321d94dba2826fd538530f7e6d060d5730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032032"
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

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесиземодечанжед.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

