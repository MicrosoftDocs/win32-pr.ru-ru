---
description: Функция Extract извлекает файлы из CAB-файла.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Извлечение функции
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162068"
---
# <a name="extract-function"></a>Извлечение функции

\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]

Функция **Extract** извлекает файлы из CAB-файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PS* 
</dt> <dd>

Указатель на структуру [**сеанса**](session.md) , содержащую сведения о текущем сеансе.

</dd> <dt>

*лпкабнаме* 
</dt> <dd>

Указатель на имя CAB-файла, из которого должны быть извлечены файлы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение **\_ ОК**; в противном случае возвращается код ошибки.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**делетикстрактедфилес**](deleteextractedfiles.md)
</dt> <dt>

[**ИНТЕГРИРОВАН**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**СЕССИИ**](session.md)
</dt> </dl>

 

 
