---
description: Закрывает указанный элемент данных из защищенного хранилища.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'Метод Ипсторе:: Клосеитем (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668483"
---
# <a name="ipstorecloseitem-method"></a>Метод Ипсторе:: Клосеитем

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Закрывает указанный элемент данных из защищенного хранилища.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Указывает, является ли тип локальным для компьютера или связан только с созданием пользователя.



| Значение                                                                                                                                                                                                                                                   | Значение                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt> </dl>    | Хранилище сохраняется в разделе реестра текущего пользователя.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt> </dl> | Хранилище сохраняется в разделе реестра локальный компьютер.<br/> |



 

</dd> <dt>

*питемтипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , определяющий тип данных закрываемого элемента.

</dd> <dt>

*питемсубтипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , указывающий подтип элемента для закрытия.

</dd> <dt>

*сзитемнаме* \[ окне\]
</dt> <dd>

Строка, содержащая имя закрываемого элемента.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Reserved: значение должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT** . Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
