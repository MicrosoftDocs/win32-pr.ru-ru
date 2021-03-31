---
title: Структура MCI_OVLY_LOAD_PARMS (Ммсистем. h)
description: '\_ \_ Структура ПАРМС загрузки MCI овли \_ содержит сведения для \_ команды MCI Load для устройств наложения видео.'
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071094"
---
# <a name="mci_ovly_load_parms-structure"></a>\_ \_ Структура ПАРМС загрузки MCI овли \_

Структура **\_ \_ \_ пармс загрузки MCI овли** содержит сведения для команды [**MCI \_ Load**](mci-load.md) для устройств наложения видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**лпфиленаме**
</dt> <dd>

Имя загружаемого файла.

</dd> <dt>

**RC**
</dt> <dd>

Определяет область обновляемого буфера видео. Структуры [Rect](/previous-versions//ms536136(v=vs.85)) в MCI обрабатываются по-разному, чем в других частях Windows. в MCI, **RC. Right** содержит ширину прямоугольника и **RC. Bottom** содержит его высоту.

</dd> </dl>

## <a name="remarks"></a>Комментарии

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

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

[**\_Загрузка MCI**](mci-load.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[ПЕРЕТАСКИВАЕМЫЕ](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

