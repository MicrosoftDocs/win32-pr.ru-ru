---
description: Удаляет объект индексированного атрибута из коллекции.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Метод Attributes. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668908"
---
# <a name="attributesremove-method"></a>Метод Attributes. Remove

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **Remove** удаляет объект индексированного [**атрибута**](attribute.md) из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Индекс удаляемого объекта [**атрибута**](attribute.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Приложения, использующие этот метод, должны содержать код, обрабатывающий исключение, вызванное этим методом.

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

 

 
