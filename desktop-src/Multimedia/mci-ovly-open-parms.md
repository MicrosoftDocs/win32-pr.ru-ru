---
title: Структура MCI_OVLY_OPEN_PARMS (Ммсистем. h)
description: '\_ \_ Структура овли Open ПАРМС в MCI \_ содержит сведения о команде MCI \_ Open для устройств наложения видео.'
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488988"
---
# <a name="mci_ovly_open_parms-structure"></a>\_Структура MCI овли \_ Open \_ пармс

Структура **\_ овли \_ Open \_ пармс в MCI** содержит сведения о команде [**MCI \_ Open**](mci-open.md) для устройств наложения видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**вдевицеид**
</dt> <dd>

Идентификатор, возвращенный приложению.

</dd> <dt>

**лпстрдевицетипе**
</dt> <dd>

Имя или идентификатор константы типа устройства. (Обычно имя устройства берется из реестра или файла SYSTEM.INI.) Если этот член является константой, это может быть одно из значений, перечисленных в [типах устройств MCI](mci-device-types.md).

</dd> <dt>

**лпстрелементнаме**
</dt> <dd>

Имя элемента устройства (обычно путь).

</dd> <dt>

**лпстралиас**
</dt> <dd>

Необязательный псевдоним устройства.

</dd> <dt>

**двстиле**
</dt> <dd>

Стиль окна.

</dd> <dt>

**хвндпарент**
</dt> <dd>

Маркер родительского окна.

</dd> </dl>

## <a name="remarks"></a>Комментарии

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

Структуру [**\_ \_ пармс для MCI**](mci-open-parms.md) можно использовать вместо **MCI \_ овли \_ Open \_ пармс** , если вы не используете расширенные элементы данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ открыт**](mci-open.md)
</dt> <dt>

[**MCI \_ Open \_ пармс**](mci-open-parms.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

