---
description: Задает или получает значение атрибута.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Свойство Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773708"
---
# <a name="attributevalue-property"></a>Свойство Attribute. Value

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Свойство **value** задает или получает значение атрибута.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Значение свойства

Переменная **типа Variant** , которая содержит значение атрибута. Для **атрибутов \_ \_ \_ \_ времени подписи атрибутов CAPICOM, прошедших проверку** , тип данных — **Date**. Для всех остальных атрибутов значением свойства является строка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
