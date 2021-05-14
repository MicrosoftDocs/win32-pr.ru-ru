---
description: Возвращает текущее использование диска пользователем в байтах.
title: Дидисккуотаусер. Куотаусед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841575"
---
# <a name="didiskquotauserquotaused-property"></a>Дидисккуотаусер. Куотаусед, свойство

Возвращает текущее использование диска пользователем в байтах.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Значение свойства

**Целочисленное** значение, которое задается как количество места на диске, используемое в данный момент. Если включено сжатие файлов NTFS, **куотаусед** отражает объем дискового пространства, требуемого для данных в несжатом состоянии.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дидисккуотаусер**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**куотасрешолд**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**куотауседтекст**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




