---
description: Эта функция получает версию библиотеки автономных разделов реестра.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Функция Оржетверсион (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648763"
---
# <a name="orgetversion-function"></a>Функция Оржетверсион

Эта функция получает версию библиотеки автономных разделов реестра.

## <a name="syntax"></a>Синтаксис


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдвмажорверсион* \[ заполняет\]
</dt> <dd>

Указатель на переменную для получения основной версии библиотеки автономного реестра. Для первоначального выпуска библиотеки значение равно 1.

</dd> <dt>

*пдвминорверсион* \[ заполняет\]
</dt> <dd>

Указатель на переменную для получения дополнительной версии библиотеки автономных разделов реестра. Для первоначального выпуска библиотеки значение равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Автономная библиотека реестра Windows версии 1,0 или более поздней<br/>                      |
| Header<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




