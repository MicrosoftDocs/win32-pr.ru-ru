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
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538366"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбкреатедатабасе**](sdbcreatedatabase.md)
</dt> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




