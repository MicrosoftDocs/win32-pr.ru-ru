---
description: Представляет тип пути, используемого в качестве аргумента.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Перечисление PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058604"
---
# <a name="path_type-enumeration"></a>\_Перечисление типов путей

Представляет тип пути, используемого в качестве аргумента.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**\_путь к DOS**
</dt> <dd>

Стандартный путь.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**\_путь NT**
</dt> <dd>

Внутренний путь.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбкреатедатабасе**](sdbcreatedatabase.md)
</dt> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




