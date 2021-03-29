---
description: Загружает библиотеку.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: Функция _LoadLibrary
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648024"
---
# <a name="_loadlibrary-function"></a>\_LoadLibrary, функция

\[Эта функция является оболочкой для функции **LoadLibrary** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **LoadLibrary** напрямую.\]

Загружает библиотеку. См. раздел [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).

## <a name="syntax"></a>Синтаксис


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
