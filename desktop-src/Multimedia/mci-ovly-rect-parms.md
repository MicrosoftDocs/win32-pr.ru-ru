---
title: Структура MCI_OVLY_RECT_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI овли Rect \_ содержит сведения о размещении для MCI \_ и MCI, \_ где команды для устройств с наложением видео.'
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- структура MCI_OVLY_RECT_PARMS Windows мультимедиа
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
ms.openlocfilehash: 5cfd55b2950f6d4268a9af5ee5bdc7fc9c378c4dbaeaa569406339263a2cf85e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039114"
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

Прямоугольник, содержащий сведения о размещении. Структуры [Rect](/previous-versions//ms536136(v=vs.85)) в MCI обрабатываются по-разному, чем в других частях Windows; в MCI, **RC. Right** содержит ширину прямоугольника и **RC. Bottom** содержит его высоту.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

