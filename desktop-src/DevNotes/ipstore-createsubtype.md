---
description: Создает указанный подтип в указанном типе.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Метод Ипсторе:: Креатесубтипе (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647998"
---
# <a name="ipstorecreatesubtype-method"></a>Метод Ипсторе:: Креатесубтипе

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Создает указанный подтип в указанном типе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSubtype(
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

Указывает область хранилища поставщика.



| Значение                                                                                                                                                                                                                                                   | Значение                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt> </dl>    | Хранилище сохраняется в разделе реестра текущего пользователя.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt> </dl> | Хранилище сохраняется в разделе реестра локальный компьютер.<br/> |



 

</dd> <dt>

*птипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , определяющий тип данных хранилища.

</dd> <dt>

*псубтипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , определяющий подтип данных хранилища.

</dd> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Указатель на структуру файла [**. \_ PST**](pst-typeinfo.md) .

</dd> <dt>

*прулес* \[ окне\]
</dt> <dd>

Указатель на структуру [**PST \_ акцессрулесет**](pst-accessruleset.md) .

**Windows XP:** Этот параметр не учитывается.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Процессу необходимо задать значение 0.

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
</dt> <dt>

[**PST-файл \_ акцессрулесет**](pst-accessruleset.md)
</dt> <dt>

[**файл \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
