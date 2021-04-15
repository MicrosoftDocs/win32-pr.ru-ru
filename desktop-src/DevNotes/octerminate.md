---
description: Закрывает диспетчер OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Функция Октерминате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648083"
---
# <a name="octerminate-function"></a>Функция Октерминате

Закрывает диспетчер OC.

## <a name="syntax"></a>Синтаксис


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Окманажерконтекст* \[ в, out\]
</dt> <dd>

На входе содержит указатель контекста диспетчера OC, возвращенный [**оЦинитиализе**](ocinitialize.md). На выходе получает **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**оЦинитиализе**](ocinitialize.md)
</dt> </dl>

 

 
