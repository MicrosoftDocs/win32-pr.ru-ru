---
description: Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Дидисккуотаусер. Куотасрешолдтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ca2136936d45850726e64b61c4fae62889d2b5e5ea30cd2b9c3a98357006e962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224679"
---
# <a name="didiskquotauserquotathresholdtext-property"></a>Дидисккуотаусер. Куотасрешолдтекст, свойство

Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a>Значение свойства

Строковое значение, содержащее порог предупреждения пользователя. Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Идисккуотаусер**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**куоталимиттекст**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**куотасрешолд**](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




