---
description: Метод Клеарсаурцелист объекта Installer удаляет все сетевые источники из исходного списка.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Метод Installer. Клеарсаурцелист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16cc37556d217a217b814b5ce87cb705cd3105d4a8c2ad3f503d617aeda2cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633042"
---
# <a name="installerclearsourcelist-method"></a>Метод Installer. Клеарсаурцелист

Метод **клеарсаурцелист** объекта [**Installer**](installer-object.md) удаляет все сетевые источники из исходного списка.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ClearSourceList(
  Product,
  User
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

[**мсисаурцелистклеаралл**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Отказоустойчивость источника](source-resiliency.md)
</dt> </dl>

 

 




