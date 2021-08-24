---
title: Структура MCI_VD_PLAY_PARMS (МЦиапи. h)
description: Структура MCI \_ VD \_ Play \_ пармс содержит сведения о положении и скорости для команды MCI \_ Play для устройств видеодиск.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- структура MCI_VD_PLAY_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c2aef6915d1e3cc325d5b9f8e1c7fe176a878c2d84080b5f8a77eaf034afc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783869"
---
# <a name="mci_vd_play_parms-structure"></a>\_Структура MCI VD \_ Play \_ пармс

Структура **MCI \_ VD \_ Play \_ пармс** содержит сведения о положении и скорости для команды [**MCI \_ Play**](mci-play.md) для устройств видеодиск.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двфром**
</dt> <dd>

Расположение для воспроизведения.

</dd> <dt>

**двто**
</dt> <dd>

Расположение для воспроизведения.

</dd> <dt>

**двспид**
</dt> <dd>

Скорость воспроизведения в кадрах за секунду.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

Вы можете использовать структуру [**MCI \_ Play \_ пармс**](mci-play-parms.md) , а не **MCI \_ VD \_ Play \_ пармс** , если вы не используете расширенные элементы данных.

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

[**\_Воспроизведение MCI**](mci-play.md)
</dt> <dt>

[**MCI \_ Play \_ пармс**](mci-play-parms.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

