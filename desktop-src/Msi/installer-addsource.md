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
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651896"
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
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсисаурцелистаддсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[отказоустойчивость источника](source-resiliency.md)
</dt> </dl>

 

 




