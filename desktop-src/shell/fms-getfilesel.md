---
description: Содержит сведения о выбранном файле в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Структура FMS_GETFILESEL (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990831"
---
# <a name="fms_getfilesel-structure"></a>\_Структура FMS жетфилесел

Содержит сведения о выбранном файле в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Участники

<dl> <dt>

**фттиме**
</dt> <dd>

Тип: **fileTime**

</dd> <dd>

Дата и время создания файла.

</dd> <dt>

**двсизе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер файла в байтах.

</dd> <dt>

**баттр**
</dt> <dd>

Тип: **Byte**

</dd> <dd>

Атрибуты файла.

</dd> <dt>

**szName**
</dt> <dd>

Тип: **TCHAR**

</dd> <dd>

Полный путь и имя файла выбранного файла, заканчивающиеся нулем.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 




