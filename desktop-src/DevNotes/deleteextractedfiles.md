---
description: Функция Делетикстрактедфилес удаляет файлы, извлеченные функцией Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Функция Делетикстрактедфилес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657215"
---
# <a name="deleteextractedfiles-function"></a>Функция Делетикстрактедфилес

\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]

Функция **делетикстрактедфилес** удаляет файлы, извлеченные функцией [**Extract**](extract.md) .

## <a name="syntax"></a>Синтаксис


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ps* 
</dt> <dd>

Указатель на структуру [**сеанса**](session.md) , содержащую сведения о текущем сеансе.

Эта функция освобождает память в элементе **пфилелист** этой структуры и задает для **пфилелист** **значение NULL**.

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

[**Распаковк**](extract.md)
</dt> <dt>

[**СЕССИИ**](session.md)
</dt> </dl>

 

 
