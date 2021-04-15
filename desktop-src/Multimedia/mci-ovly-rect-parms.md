---
title: Структура MCI_OVLY_RECT_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI овли Rect \_ содержит сведения о размещении для MCI \_ и MCI, \_ где команды для устройств с наложением видео.'
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488985"
---
# <a name="mci_ovly_rect_parms-structure"></a>\_Структура пармс для MCI овли \_ Rect \_

Структура **\_ \_ \_ пармс MCI овли Rect** содержит сведения о размещении для [**MCI \_**](mci-put.md) и [**MCI, \_ где**](mci-where.md) команды для устройств с наложением видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**RC**
</dt> <dd>

Прямоугольник, содержащий сведения о размещении. Структуры [Rect](/previous-versions//ms536136(v=vs.85)) в MCI обрабатываются по-разному, чем в других частях Windows. в MCI, **RC. Right** содержит ширину прямоугольника и **RC. Bottom** содержит его высоту.

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

[**\_Добавление MCI**](mci-put.md)
</dt> <dt>

[**MCI, \_ где**](mci-where.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[ПЕРЕТАСКИВАЕМЫЕ](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

