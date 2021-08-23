---
description: Перезагружает конфигурацию редактора IME из реестра HKCU в японском РЕДАКТОРЕ.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: Функция reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571624"
---
# <a name="reload_config-function"></a>перезагрузка \_ функции конфигурации

Перезагружает конфигурацию редактора IME из реестра HKCU в японском РЕДАКТОРЕ.

## <a name="syntax"></a>Синтаксис


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Если в HKCU не указано значение реестра, функция **перезагрузки \_ конфигурации** записывает исходные данные в реестр.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
