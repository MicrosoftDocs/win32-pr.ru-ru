---
description: Возвращает указатель интерфейса подтипа для перечисления элементов в защищенной базе данных хранилища.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Метод Ипсторе:: Енумитемс (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648096"
---
# <a name="ipstoreenumitems-method"></a>Метод Ипсторе:: Енумитемс

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Возвращает указатель интерфейса подтипа для перечисления элементов в защищенной базе данных хранилища.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
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

Указатель на **идентификатор GUID** , определяющий тип данных элемента для перечисления.

</dd> <dt>

*питемсубтипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , определяющий подтип данных элемента для перечисления.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Reserved: значение должно быть равно нулю.

</dd> <dt>

*ппенум* \[ окне\]
</dt> <dd>

Указатель на указатель на интерфейс [**иенумпстореитемс**](ienumpstoreitems.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> </dl>

 

 
