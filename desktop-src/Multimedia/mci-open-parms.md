---
title: Структура MCI_OPEN_PARMS (МЦиапи. h)
description: Структура MCI \_ Open \_ пармс содержит сведения для \_ команды MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- структура MCI_OPEN_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138309"
---
# <a name="mci_open_parms-structure"></a>\_Структура Open \_ ПАРМС для MCI

Структура **MCI \_ Open \_ пармс** содержит сведения для команды [**MCI \_ Open**](mci-open.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
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

Элемент Device (часто путь).

</dd> <dt>

**лпстралиас**
</dt> <dd>

Необязательный псевдоним устройства.

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

[**MCI \_ открыт**](mci-open.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

