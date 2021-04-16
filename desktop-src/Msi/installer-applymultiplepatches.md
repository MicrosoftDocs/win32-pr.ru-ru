---
description: Метод Апплимултиплепатчес применяет один или несколько исправлений к продуктам, которые могут получить исправление. Метод задает свойство PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Метод Installer. Апплимултиплепатчес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651913"
---
# <a name="installerapplymultiplepatches-method"></a>Метод Installer. Апплимултиплепатчес

Метод **апплимултиплепатчес** применяет один или несколько исправлений к продуктам, которые могут получить исправление. Метод задает свойство [**Patch**](patch.md) .

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*патчпаккажеслист* 
</dt> <dd>

Строка, содержащая разделенный точками с запятой список путей к файлам исправлений. Например: "" c: \\ \\ кэш скачивания SUS \\ \\ Office \\ с пакетом обновления 1 (SP1). MSP; в. \\ \\ скачивание с \\ \\ пакетом обновления Office \\ QFE1. MSP; c: \\ SUS \\ download \\ кэша \\ Office \\ кфен. MSP ""

</dd> <dt>

*Продукт* 
</dt> <dd>

Этот параметр предоставляет [**код**](productcode.md) продукта для исправления. Это необязательный параметр. Если этот параметр имеет значение null, исправления применяются ко всем продуктам, которые могут принимать эти исправления.

</dd> <dt>

*сзпропертиеслист* 
</dt> <dd>

Строка, завершающаяся нулем, которая задает параметры свойства командной строки. Это необязательный параметр. См. раздел [о свойствах](about-properties.md) и [Установка значений общих свойств в командной строке](setting-public-property-values-on-the-command-line.md). Эти свойства являются общими для всех целевых продуктов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения о свойствах](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**PATCH**](patch.md)
</dt> <dt>

[Установка значений открытых свойств в командной строке](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




