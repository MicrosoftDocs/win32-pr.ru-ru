---
description: Предназначен для установки указанных сведений о параметрах.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Метод Ипсторе:: Жетпровпарам (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955913"
---
# <a name="ipstoregetprovparam-method"></a>Метод Ипсторе:: Жетпровпарам

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Этот метод не реализован.\]

Предназначен для установки указанных сведений о параметрах. Однако обратите внимание, что она не реализована и всегда завершается ошибкой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпарам* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*пкбдата* \[ заполняет\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*ппбдата* \[ заполняет\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Вызовы этого метода всегда завершатся ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
