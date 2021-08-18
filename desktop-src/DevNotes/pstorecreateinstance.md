---
description: Извлекает указатель интерфейса на поставщик хранилища.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Функция Псторекреатеинстанце (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955693"
---
# <a name="pstorecreateinstance-function"></a>Функция Псторекреатеинстанце

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Эта функция может быть изменена или недоступна в будущих версиях Windows. Вместо этой функции используйте функции **CryptProtectData** и **CryptUnprotectData** .\]

Извлекает указатель интерфейса на поставщик хранилища.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пппровидер* \[ заполняет\]
</dt> <dd>

Указатель на полученный указатель интерфейса для поставщика хранилища. По завершении использования интерфейса уменьшите его число ссылок, вызвав метод [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*ппровидерид* \[ окне\]
</dt> <dd>

Указатель на **идентификатор GUID** , который идентифицирует поставщик хранилища. Если этот параметр имеет **значение NULL**, используется базовый поставщик хранилища.

</dd> <dt>

*сохраняется* \[ окне\]
</dt> <dd>

Процессу должен иметь **значение NULL**.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Процессу должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение **S \_ ОК** указывает, что функция выполнена успешно.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта; его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
