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
ms.openlocfilehash: a9225799eeb7d093d706dcb7063f998a2813eab4b2117e2ca776244e4fcf72a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679613"
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



## <a name="members"></a>Члены

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> <dt>

[**FM \_ жетдривеинфо**](fm-getdriveinfo.md)
</dt> </dl>

 

 




