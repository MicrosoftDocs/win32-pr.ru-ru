---
description: Получает логическое значение, указывающее, имеется ли расширение базовых ограничений. Это свойство по умолчанию.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: Басикконстраинтс. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665529"
---
# <a name="basicconstraintsispresent-property"></a>Басикконстраинтс. Present, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

Свойство **Present** получает логическое значение, указывающее, имеется ли расширение базовых ограничений. Это свойство по умолчанию.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение — true**, имеется расширение базовых ограничений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**басикконстраинтс**](basicconstraints.md)
</dt> </dl>

 

 
