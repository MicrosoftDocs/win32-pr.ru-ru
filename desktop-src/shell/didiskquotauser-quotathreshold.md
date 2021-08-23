---
description: Задает или возвращает порог предупреждения пользователя в байтах.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Дидисккуотаусер. Куотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 38caa5ef5ded6ed40708314c6063fba13a74cbbe506465aed55e8504898a9307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032792"
---
# <a name="didiskquotauserquotathreshold-property"></a>Дидисккуотаусер. Куотасрешолд, свойство

Задает или возвращает порог предупреждения пользователя в байтах.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>Значение свойства

**Целочисленное** значение, указывающее или получающее порог предупреждения пользователя. Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**дефаулткуотасрешолд**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**дидисккуотаусер**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**куотасрешолдтекст**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




