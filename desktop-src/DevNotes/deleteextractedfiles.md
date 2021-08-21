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
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162095"
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

*PS* 
</dt> <dd>

Указатель на структуру [**сеанса**](session.md) , содержащую сведения о текущем сеансе.

Эта функция освобождает память в элементе **пфилелист** этой структуры и задает для **пфилелист** **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Распаковк**](extract.md)
</dt> <dt>

[**СЕССИИ**](session.md)
</dt> </dl>

 

 
