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
ms.openlocfilehash: 399bdb936befb4f7ff45f9f5a3b132245b984bf2a5201ce054ee0fbeb50f5598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833354"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**оЦинитиализе**](ocinitialize.md)
</dt> </dl>

 

 
