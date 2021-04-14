---
description: Возвращает уровень правила идентификации хэша, соответствующего указанному хэшу.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Функция Саферисеарчматчингхашрулес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496488"
---
# <a name="saferisearchmatchinghashrules-function"></a>Функция Саферисеарчматчингхашрулес

Возвращает уровень правила идентификации хэша, соответствующего указанному хэшу.

Эта функция не имеет связанной библиотеки импорта и не объявлена в общедоступном заголовке. Необходимо определить указатель функции с сигнатурой этой функции, и для динамической привязки к Advapi32.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Для вычисления политик ограниченного использования программ рекомендуется использовать функцию [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HashAlgorithm* \[ в необязательное\]
</dt> <dd>

Идентификатор алгоритма, используемого для создания хэша.

</dd> <dt>

*фашбитес* \[ окне\]
</dt> <dd>

Указатель на массив байтов, содержащий хэш.

</dd> <dt>

*двхашсизе* \[ окне\]
</dt> <dd>

Размер массива *фашбитес* в байтах.

</dd> <dt>

*дворигиналимажесизе* \[ в необязательное\]
</dt> <dd>

Размер (в байтах) исходного изображения, из которого был вычислен хэш.

</dd> <dt>

*пдвфаундлевел* \[ заполняет\]
</dt> <dd>

Указатель на идентификатор уровня для соответствующего правила идентификации хэш-кода.

</dd> <dt>

*пдвсаферфлагс* 
</dt> <dd>

Зарезервировано. Присвойте этому параметру значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если функция выполнена успешно; в противном случае — **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
