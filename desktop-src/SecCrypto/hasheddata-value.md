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
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665314"
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

## <a name="remarks"></a>Комментарии

Чтобы создать хэш большого объема данных, вызовите метод [**хэширования**](hasheddata-hash.md) для каждого фрагмента данных. Хэш каждого фрагмента данных объединяется со свойством **value** до тех пор, пока свойство не будет считано. Содержимое свойства **value** сбрасывается при считывании свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**хашеддата**](hasheddata.md)
</dt> </dl>

 

 
