---
description: Создает другой перечислитель с тем же состоянием перечисления, что и текущий.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'Метод Иенумпсторепровидерс:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648804"
---
# <a name="ienumpstoreprovidersclone-method"></a>Метод Иенумпсторепровидерс:: Clone

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Создает другой перечислитель с тем же состоянием перечисления, что и текущий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* \[ заполняет\]
</dt> <dd>

Указатель на указатель [**иенумпсторепровидерс**](ienumpstoreproviders.md) .

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

 

 
