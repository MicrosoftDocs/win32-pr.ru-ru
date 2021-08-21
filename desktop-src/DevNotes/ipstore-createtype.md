---
description: Создает указанный тип с указанным именем.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'Метод Ипсторе:: CreateType (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7064cd07c0af99cbb325457217c2679757837be3ac1f5d80977cd2bb222f6b75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667522"
---
# <a name="ipstorecreatetype-method"></a>Метод Ипсторе:: CreateType

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Создает указанный тип с указанным именем.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
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

*птипе* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , определяющий тип данных хранилища.

</dd> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Указатель на структуру файла [**. \_ PST**](pst-typeinfo.md) , содержащий имя типа данных.

</dd> <dt>

*dwFlags* \[ окне\]
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипсторе**](ipstore.md)
</dt> <dt>

[**файл \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
