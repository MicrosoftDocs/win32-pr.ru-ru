---
description: 'Метод Иенумпсторетипес:: Skip — пропускает следующее заданное число элементов в последовательности перечисления.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Метод Иенумпсторетипес:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: bcd1d6eb0f348bc74ac44f054bba9c7cd792158f984b8f6a920c91ee06e7d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827222"
---
# <a name="ienumpstoretypesskip-method"></a>Метод Иенумпсторетипес:: Skip

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Пропускает следующее заданное число элементов в последовательности перечисления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*celt* \[ окне\]
</dt> <dd>

Число типов поставщиков для пропуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумпсторетипес**](ienumpstoretypes.md)
</dt> </dl>

 

 
