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
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843215"
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

## <a name="requirements"></a>Requirements (Требования)



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

 

 




