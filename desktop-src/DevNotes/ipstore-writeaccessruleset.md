---
description: Записывает правила доступа для заданного типа.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'Метод Ипсторе:: Вритеакцессрулесет (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955903"
---
# <a name="ipstorewriteaccessruleset-method"></a>Метод Ипсторе:: Вритеакцессрулесет

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Этот метод не реализован.\]

Записывает правила доступа для заданного типа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
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

*прулес* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Вызовы этого метода всегда завершатся ошибкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
