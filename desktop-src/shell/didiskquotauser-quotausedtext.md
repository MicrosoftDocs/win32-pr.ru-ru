---
description: Возвращает текущий объем использования диска пользователем в виде текстовой строки.
title: Дидисккуотаусер. Куотауседтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984264"
---
# <a name="didiskquotauserquotausedtext-property"></a>Дидисккуотаусер. Куотауседтекст, свойство

Возвращает текущий объем использования диска пользователем в виде текстовой строки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Значение свойства

Строковое значение, заданное как объем используемого места на диске. Если включено сжатие файлов NTFS, это свойство отражает объем места на диске, требуемый для данных в несжатом состоянии.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дидисккуотаусер**](didiskquotauser-object.md)
</dt> <dt>

[**куоталимиттекст**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**куотасрешолдтекст**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




