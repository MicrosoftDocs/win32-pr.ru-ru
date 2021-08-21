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
ms.openlocfilehash: 2828f54f754591d1b0027a6c892dc57e8b5cdfecc5e9759985b74b1dffef9fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006582"
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

## <a name="remarks"></a>Remarks

Чтобы создать хэш большого объема данных, вызовите метод **хэширования** для каждого фрагмента данных. Хэш каждого фрагмента данных объединяется со свойством [**value**](hasheddata-value.md) до тех пор, пока свойство не будет считано. Содержимое свойства **value** сбрасывается при считывании свойства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
