---
description: Пропускает следующее заданное число элементов в последовательности перечисления.
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
ms.openlocfilehash: 75ec981e76d387f6ada82869bba40fa4946ce7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657089"
---
# <a name="ienumpstoreprovidersskip-method"></a>Метод Иенумпсторепровидерс:: Skip

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумпсторепровидерс**](ienumpstoreproviders.md)
</dt> </dl>

 

 
