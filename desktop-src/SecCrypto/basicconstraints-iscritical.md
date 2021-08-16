---
description: Получает логическое значение, указывающее, помечено ли расширение базового ограничения как критическое.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Свойство Басикконстраинтс. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3918a89719195e6c8672a0dab13c62af3e866f8fd5695df20f0126f7831f369c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773036"
---
# <a name="basicconstraintsiscritical-property"></a>Свойство Басикконстраинтс. Critical

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение базового ограничения как критическое.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение — true**, расширение базового ограничения помечается как критическое.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
