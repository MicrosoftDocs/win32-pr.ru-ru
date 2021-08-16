---
description: Метод Аддсаурце объекта Installer добавляет источник в список допустимых сетевых источников в списке.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Метод Installer. Аддсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c5e2b87a1fc9a660ae835d9fb1cfa465673bb6698144a9695cbfb264535a948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633170"
---
# <a name="installeraddsource-method"></a>Метод Installer. Аддсаурце

Метод **аддсаурце** объекта [**Installer**](installer-object.md) добавляет источник в список допустимых сетевых источников в списке.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Продукт* 
</dt> <dd>

Указывает код продукта.

</dd> <dt>

*Пользователь* 
</dt> <dd>

Имя пользователя для установки на уровне пользователя; значение null или пустая строка для установки на компьютере.

</dd> <dt>

*Источник* 
</dt> <dd>

Указатель на строку, указывающую источник.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсисаурцелистаддсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[отказоустойчивость источника](source-resiliency.md)
</dt> </dl>

 

 




