---
description: Создает хэш указанной строки.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Хашеддата. hash, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665315"
---
# <a name="hasheddatahash-method"></a>Хашеддата. hash, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **hash** создает хэш указанной строки.

## <a name="syntax"></a>Синтаксис


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* 
</dt> <dd>

Строка, содержащая значение для хэширования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Чтобы создать хэш большого объема данных, вызовите метод **хэширования** для каждого фрагмента данных. Хэш каждого фрагмента данных объединяется со свойством [**value**](hasheddata-value.md) до тех пор, пока свойство не будет считано. Содержимое свойства **value** сбрасывается при считывании свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
