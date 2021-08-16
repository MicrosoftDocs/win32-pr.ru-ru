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
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633211"
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

Строка, содержащая разделенный точками с запятой список путей к файлам исправлений. например: "" c: \\ \\ кэш скачивания sus \\ \\ Office \\ sp1. msp; в. \\ \\ скачивание \\ кэша sus \\ Office \\ QFE1. msp; c: \\ sus \\ download \\ cache \\ Office \\ кфен. msp ""

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
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения о свойствах](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**ЗАЩИТЫ**](patch.md)
</dt> <dt>

[Установка значений открытых свойств в командной строке](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




