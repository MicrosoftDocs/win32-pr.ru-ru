---
description: Освобождает дескриптор поставщика служб шифрования (CSP) и при необходимости удаляет временный контейнер, созданный функцией Пвкжеткриптпров.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Функция Пвкфрикриптпров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684334"
---
# <a name="pvkfreecryptprov-function"></a>Функция Пвкфрикриптпров

> [!IMPORTANT]
> Это нерекомендуемый API. Корпорация Майкрософт может удалить этот API в будущих выпусках.

 

Функция **пвкфрикриптпров** освобождает дескриптор [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и при необходимости удаляет временный контейнер, созданный функцией [**пвкжеткриптпров**](pvkgetcryptprov.md) .

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпров* \[ окне\]
</dt> <dd>

Маркер для CSP.

</dd> <dt>

*пвсзкапипровидер* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, для имени CSP.

</dd> <dt>

*двпровидертипе* \[ окне\]
</dt> <dd>

Значение типа **DWORD** , представляющее тип поставщика служб шифрования. Дополнительные сведения см. в разделе [типы поставщиков служб шифрования](cryptographic-provider-types.md).

</dd> <dt>

*пвсзтмпконтаинер* \[ в необязательное\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, для имени контейнера временного ключа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
