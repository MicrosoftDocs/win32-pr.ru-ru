---
description: Инициализирует таблицу строк.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Функция Псетупстрингтаблеинитиализикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665252"
---
# <a name="psetupstringtableinitializeex-function"></a>Функция Псетупстрингтаблеинитиализикс

\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]

Инициализирует таблицу строк.

## <a name="syntax"></a>Синтаксис


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Екстрадатасизе* \[ окне\]
</dt> <dd>

Размер дополнительного объекта данных.

</dd> <dt>

*Зарезервировано* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
