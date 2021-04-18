---
description: Закрывает указанный куст автономного реестра и освобождает память, выделенную для Hive.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Функция Орклосехиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649011"
---
# <a name="orclosehive-function"></a>Функция Орклосехиве

Закрывает указанный куст автономного реестра и освобождает память, выделенную для Hive.

## <a name="syntax"></a>Синтаксис


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обработчик* \[ окне\]
</dt> <dd>

Маркер корневого ключа автономного куста реестра, который необходимо закрыть.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.

## <a name="remarks"></a>Комментарии

Функция **орклосехиве** освобождает всю память, выделенную автономными функциями реестра от имени указанного Hive.

Чтобы сохранить изменения в Hive, вызовите функцию [**орсавехиве**](orsavehive.md) перед вызовом **орклосехиве**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Автономная библиотека реестра Windows версии 1,0 или более поздней<br/>                      |
| Header<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**оропенхиве**](oropenhive.md)
</dt> <dt>

[**орсавехиве**](orsavehive.md)
</dt> </dl>

 

 
