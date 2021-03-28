---
description: Возвращает логическое значение, указывающее, выполняется ли перестроение файла квоты для тома.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Дисккуотаконтрол. Куотафилеребуилдинг, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984412"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Дисккуотаконтрол. Куотафилеребуилдинг, свойство

Возвращает логическое значение, указывающее, выполняется ли перестроение файла квоты для тома.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Значение свойства

Это свойство имеет значение **true** , если выполняется перестроение файла квоты, или **false** в противном случае.

## <a name="remarks"></a>Примечания

Файл квоты автоматически перестраивается, когда квоты включены в системе или если одна или несколько записей пользователя помечены для удаления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




