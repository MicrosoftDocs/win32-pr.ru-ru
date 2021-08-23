---
description: Извлекает хэшированные данные после успешного вызова метода хэширования.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Хашеддата. Value, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a6b8b2c8291e793cd88c5d4b0821c036fb6b112beb87e73d4f8ccb8d523deb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006572"
---
# <a name="hasheddatavalue-property"></a>Хашеддата. Value, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **value** извлекает хэшированные данные после успешного вызова метода [**хэширования**](hasheddata-hash.md) . Хэш-значение возвращается в шестнадцатеричном формате. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая хэшированные данные в шестнадцатеричном формате.

## <a name="remarks"></a>Remarks

Чтобы создать хэш большого объема данных, вызовите метод [**хэширования**](hasheddata-hash.md) для каждого фрагмента данных. Хэш каждого фрагмента данных объединяется со свойством **value** до тех пор, пока свойство не будет считано. Содержимое свойства **value** сбрасывается при считывании свойства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**хашеддата**](hasheddata.md)
</dt> </dl>

 

 
