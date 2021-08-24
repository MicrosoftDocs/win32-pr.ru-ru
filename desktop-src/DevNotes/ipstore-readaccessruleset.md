---
description: Считывает правила доступа для заданного типа.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Метод Ипсторе:: Реадакцессрулесет (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d22f56c14df4d11a8979065ede81ab8418909033ffd816a233a18c51af7f66c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749754"
---
# <a name="ipstorereadaccessruleset-method"></a>Метод Ипсторе:: Реадакцессрулесет

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Этот метод не реализован.\]

Считывает правила доступа для заданного типа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*птипе* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*псубтипе* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*ппрулес* \[ окне\]
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

 

 
