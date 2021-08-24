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
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710524"
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

## <a name="remarks"></a>Remarks

Файл квоты автоматически перестраивается, когда квоты включены в системе или если одна или несколько записей пользователя помечены для удаления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




