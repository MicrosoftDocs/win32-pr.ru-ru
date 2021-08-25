---
description: Событие InkCollector. Таблетремовед — происходит при удалении Иинктаблет из системы.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Событие InkCollector. Таблетремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d3c319a4e67a22c81a74c6b5acceba7bd6f19188042fc68ebe4c7c7c8314e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773524"
---
# <a name="inkcollectortabletremoved-event"></a>Событие InkCollector. Таблетремовед

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

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицетаблетремовед.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




