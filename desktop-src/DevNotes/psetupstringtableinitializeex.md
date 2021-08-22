---
description: Функция Псетупстрингтаблеинитиализикс — инициализирует таблицу строк.
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
ms.openlocfilehash: 189bb94b70366ad66f0fe4dd4c4c9d5884e762cf20638f7c3ae2dc9b587f15ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538474"
---
# <a name="psetupstringtableinitializeex-function"></a>Функция Псетупстрингтаблеинитиализикс

\[эта функция недоступна в Windows Vista или Windows Server 2008.\]

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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
