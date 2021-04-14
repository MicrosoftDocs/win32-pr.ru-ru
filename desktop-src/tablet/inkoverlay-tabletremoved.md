---
description: Происходит при удалении Иинктаблет из системы.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: Событие InkOverlay. Таблетремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d0e69bae7cb6360794b9624fcef7c8be639e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647412"
---
# <a name="inkoverlaytabletremoved-event"></a>Событие InkOverlay. Таблетремовед

Происходит при удалении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.

## <a name="syntax"></a>Синтаксис


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Таблетид* \[ окне\]
</dt> <dd>

Значение типа Long, которое было использовано в качестве идентификатора удаленного объекта [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицетаблетремовед.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




