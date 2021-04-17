---
description: Инициализирует таблицу строк.
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
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665255"
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

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
