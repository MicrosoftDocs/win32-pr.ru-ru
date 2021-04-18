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
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648876"
---
# <a name="ipstorereadaccessruleset-method"></a>Метод Ипсторе:: Реадакцессрулесет

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
