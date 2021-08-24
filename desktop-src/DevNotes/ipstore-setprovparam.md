---
description: Задает сведения о заданных параметрах.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Метод Ипсторе:: Сетпровпарам (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9ec106cd4558ddab7fd8bc430088f1bd7d721d7122f77166dfe0da7de35f1787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749724"
---
# <a name="ipstoresetprovparam-method"></a>Метод Ипсторе:: Сетпровпарам

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Задает сведения о заданных параметрах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпарам* \[ окне\]
</dt> <dd>

Содержит **\_ кэш PST \_ PP \_ flush \_ пароль** для очистки кэша паролей пользователей.

</dd> <dt>

*cbData* \[ окне\]
</dt> <dd>

Длина пароля в буфере.

</dd> <dt>

*pbData* 
</dt> <dd>

Указатель на буфер, содержащий пароль пользователя. Это значение должно быть равно **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Reserved: значение должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT** . Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
