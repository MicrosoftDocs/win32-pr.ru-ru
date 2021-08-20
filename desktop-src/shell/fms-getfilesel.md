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
ms.openlocfilehash: 4a57aa2063af14c90cf73a21ab9331442b889aada1c979a52ff986fe92676acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679603"
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



## <a name="members"></a>Члены

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 




