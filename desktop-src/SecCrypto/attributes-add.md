---
description: Добавляет объект атрибута в коллекцию.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Метод Attributes. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5639a4bed96dcf4cef315b4550cd2982778d6ecc68024364f06eb377cbd8b0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773519"
---
# <a name="attributesadd-method"></a>Метод Attributes. Add

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Метод **Add** добавляет объект [**атрибута**](attribute.md) в коллекцию.

## <a name="syntax"></a>Синтаксис


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Атрибут* \[ окне\]
</dt> <dd>

Объект [**атрибута**](attribute.md) , добавляемый в конец коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. Приложение, использующее этот метод, должно содержать код, обрабатывающий исключение, вызванное этим методом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Атрибуты**](attributes.md)
</dt> </dl>

 

 
