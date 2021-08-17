---
description: 'Метод Иенумпсторепровидерс:: Skip — пропускает следующее заданное число элементов в последовательности перечисления.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'Метод Иенумпсторепровидерс:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73e33bb10f32a3bf2defeb2c92d9bf97d830b1c7a2b36449594ff3c62751bc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955943"
---
# <a name="ienumpstoreprovidersskip-method"></a>Метод Иенумпсторепровидерс:: Skip

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

[**иенумпсторепровидерс**](ienumpstoreproviders.md)
</dt> </dl>

 

 
