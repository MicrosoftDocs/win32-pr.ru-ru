---
title: Структура MCI_WAVE_OPEN_PARMS (МЦиапи. h)
description: Структура MCI \_ Wave \_ Open \_ пармс содержит сведения о команде MCI \_ Open для устройств аудио-Audio.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672767"
---
# <a name="mci_wave_open_parms-structure"></a>\_ \_ \_ Структура пармс для звукозаписи MCI

Структура **MCI \_ Wave \_ Open \_ пармс** содержит сведения о команде [**MCI \_ Open**](mci-open.md) для устройств аудио-Audio.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
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

Имя или идентификатор константы типа устройства. (Обычно имя устройства берется из реестра или файла SYSTEM.INI.) Этот элемент может быть одним из значений, перечисленных в [типах устройств MCI](mci-device-types.md).

</dd> <dt>

**лпстрелементнаме**
</dt> <dd>

Имя элемента устройства (обычно путь).

</dd> <dt>

**лпстралиас**
</dt> <dd>

Необязательный псевдоним устройства.

</dd> <dt>

**двбуфферсекондс**
</dt> <dd>

Длина буфера в секундах.

</dd> </dl>

## <a name="remarks"></a>Комментарии

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

Если вы не используете расширенные элементы данных, можно использовать структуру [**MCI \_ Open \_ пармс**](mci-open-parms.md) , а не звукозапись **MCI \_ \_ Open \_ пармс** .

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

[**MCI \_ открыт**](mci-open.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCI \_ Open \_ пармс**](mci-open-parms.md)
</dt> </dl>

 

