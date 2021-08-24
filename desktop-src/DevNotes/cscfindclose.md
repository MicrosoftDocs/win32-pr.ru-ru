---
description: Закрывает маркер поиска.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Функция Кскфиндклосе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 862159ed74d6c7c9ddbe4d6f97bede37bab7dca949e6d3259715737de07b8df5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758724"
---
# <a name="cscfindclose-function"></a>Функция Кскфиндклосе

\[Эта функция не поддерживается и не должна использоваться.\]

Закрывает маркер поиска.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфинд* \[ окне\]
</dt> <dd>

Маркер поиска, возвращаемый функцией [**кскфиндфирстфилев**](cscfindfirstfilew.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**кскфиндфирстфилев**](cscfindfirstfilew.md)
</dt> </dl>

 

 
