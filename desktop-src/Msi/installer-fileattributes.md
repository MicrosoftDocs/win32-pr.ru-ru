---
description: Свойство FileAttributes объекта Installer возвращает число, представляющее комбинированные атрибуты файла для указанного пути к файлу или папке.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: свойство установщика. FileAttributes (Windows. storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fe43028d856ca26b1c5e8fa21a88a3b77381670ccc044a79f10d3b922f38c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630917"
---
# <a name="installerfileattributes-property"></a>Свойство Installer. FileAttributes

Свойство **FileAttributes** объекта [**Installer**](installer-object.md) возвращает число, представляющее комбинированные атрибуты файла для указанного пути к файлу или папке.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Значение свойства

Требуемый путь к файлу или папке. Частичный путь предполагает наличие текущего каталога.

## <a name="remarks"></a>Remarks

Свойство **FileAttributes** возвращает следующие значения.



| Атрибут файла              | Значение      | Значение |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| \_ \_ временный атрибут файла  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Возвращает значение – 1, если файл или папка не существуют или недоступны.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| Header<br/>  | <dl> <dt>Windows. storage. h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




