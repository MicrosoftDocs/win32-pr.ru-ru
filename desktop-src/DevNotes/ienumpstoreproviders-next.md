---
description: Возвращает указанное число следующих поставщиков в последовательности перечисления.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'Метод Иенумпсторепровидерс:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ad35f76622abd61c6830f338a670c42a2c2f9178d0d6692044eec62621617976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691294"
---
# <a name="ienumpstoreprovidersnext-method"></a>Метод Иенумпсторепровидерс:: Next

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Возвращает указанное число следующих поставщиков в последовательности перечисления.

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

Указатель на число типов поставщиков, которые были переданы фактически.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иенумпсторепровидерс**](ienumpstoreproviders.md)
</dt> </dl>

 

 
