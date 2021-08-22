---
description: метод форцесаурцелистресолутион объекта Installer заставляет установщик Windows искать допустимый источник продукта в списке источников.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Метод Installer. Форцесаурцелистресолутион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630596"
---
# <a name="installerforcesourcelistresolution-method"></a>Метод Installer. Форцесаурцелистресолутион

Метод **форцесаурцелистресолутион** объекта [**Installer**](installer-object.md) заставляет установщик выполнять поиск действительного источника продукта в исходном списке, например, когда установщик выполняет установку или переустановку, или когда ему требуется путь для запуска набора компонентов из источника данных, если он необходим.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ForceSourceListResolution(
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

[**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Отказоустойчивость источника](source-resiliency.md)
</dt> </dl>

 

 




