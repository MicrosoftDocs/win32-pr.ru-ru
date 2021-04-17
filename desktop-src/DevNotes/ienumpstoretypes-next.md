---
description: Возвращает указанное число следующих типов поставщиков в последовательности перечисления.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Метод Иенумпсторетипес:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657899"
---
# <a name="ienumpstoretypesnext-method"></a>Метод Иенумпсторетипес:: Next

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Возвращает указанное число следующих типов поставщиков в последовательности перечисления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*celt* \[ окне\]
</dt> <dd>

Число запрошенных типов поставщиков.

</dd> <dt>

*rgelt* \[ заполняет\]
</dt> <dd>

Указатель на строку, в которой возвращается имя типа поставщика.

</dd> <dt>

*пцелтфетчед* \[ в, out\]
</dt> <dd>

Указатель на число фактически предоставляемых типов поставщиков.

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

[**иенумпсторетипес**](ienumpstoretypes.md)
</dt> </dl>

 

 
