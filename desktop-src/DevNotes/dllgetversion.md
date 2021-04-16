---
description: Функция Дллжетверсион извлекает номер версии Cabinet.dll используя структуру КАБИНЕТДЛЛВЕРСИОНИНФО.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Функция Дллжетверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648104"
---
# <a name="dllgetversion-function"></a>Функция Дллжетверсион

\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]

Функция **дллжетверсион** извлекает номер версии Cabinet.dll используя структуру [**кабинетдллверсионинфо**](cabinetdllversioninfo.md) .

## <a name="syntax"></a>Синтаксис


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкдви* 
</dt> <dd>

Указатель на структуру [**кабинетдллверсионинфо**](cabinetdllversioninfo.md) , содержащую сведения о версии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кабинетдллверсионинфо**](cabinetdllversioninfo.md)
</dt> <dt>

[**жетдллверсион**](getdllversion.md)
</dt> </dl>

 

 
