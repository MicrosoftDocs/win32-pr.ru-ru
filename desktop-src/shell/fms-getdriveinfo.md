---
description: Содержит сведения о диске, выбранном в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Структура FMS_GETDRIVEINFO (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985509"
---
# <a name="fms_getdriveinfo-structure"></a>\_Структура FMS жетдривеинфо

Содержит сведения о диске, выбранном в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Участники

<dl> <dt>

**двтоталспаце**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Общий объем дискового пространства (в байтах) на диске, связанном с диском.

</dd> <dt>

**двфриспаце**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Объем свободного дискового пространства (в байтах) на диске, связанном с диском.

</dd> <dt>

**сзпас**
</dt> <dd>

Тип: **TCHAR \[ 260 \]**

</dd> <dd>

путь к текущему каталогу, заканчивающийся нулем.

</dd> <dt>

**сзволуме**
</dt> <dd>

Тип: **TCHAR \[ 14 \]**

</dd> <dd>

Метка тома, завершающаяся нулем, для диска, связанного с диском.

</dd> <dt>

**сзшаре**
</dt> <dd>

Тип: **TCHAR \[ 128 \]**

</dd> <dd>

Имя сетевого ресурса, заканчивающееся нулем (если доступ к диску осуществляется по сети).

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
</dt> <dt>

[**FM \_ жетдривеинфо**](fm-getdriveinfo.md)
</dt> </dl>

 

 




