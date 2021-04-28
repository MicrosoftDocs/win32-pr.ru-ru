---
description: Функция Псетупстрингтаблеинитиализе — инициализирует таблицу строк.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: Функция Псетупстрингтаблеинитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089203"
---
# <a name="psetupstringtableinitialize-function"></a>Функция Псетупстрингтаблеинитиализе

\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]

Инициализирует таблицу строк.

## <a name="syntax"></a>Синтаксис


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
