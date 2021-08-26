---
description: Извлекает сведения о загруженном в данный момент наборе модулей для системы.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Функция Ауксклибкуеримодулеинформатион (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045322"
---
# <a name="auxklibquerymoduleinformation-function"></a>Функция Ауксклибкуеримодулеинформатион

Извлекает сведения о загруженном в данный момент наборе модулей для системы.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*BufferSize* \[ в, out\]
</dt> <dd>

На входе — размер буфера *куеринфо* в байтах. На выходе получает фактический требуемый размер. Так как список системных модулей может изменяться между вызовами, это значение также может изменяться между вызовами.

</dd> <dt>

*ElementSize* \[ окне\]
</dt> <dd>

Размер элемента массива в байтах. Этот размер определяет формат выходных данных.

</dd> <dt>

*Куеринфо* \[ out, необязательно\]
</dt> <dd>

Указатель на буфер, который получает сведения о модуле. Эти сведения возвращаются в массиве, элементы которого являются одной из следующих структур: дополнительная информация о вспомогательном [**\_ модуле \_ \_**](aux-module-basic-info-struct.md) или [**\_ \_ Расширенные \_ сведения о модуле AUX**](aux-module-extended-info-struct.md). Конкретная используемая структура зависит от указанного размера элемента.

Если этот параметр имеет **значение NULL**, функция возвращает требуемый размер буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение STATUS \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть одним из кодов состояния, определенных в файле Ntstatus. h, который доступен в WDK.

## <a name="remarks"></a>Remarks

Перед вызовом этой функции необходимо вызвать функцию [**ауксклибинитиализе**](auxklibinitialize-func.md) .

Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|------------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Windows Вспомогательная библиотека API версии 1,0 или более поздней<br/>                            |
| Заголовок<br/>          | <dl> <dt>AUX \_ клиб. h</dt> </dl>   |
| Библиотека<br/>         | <dl> <dt>AUX \_ клиб. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ауксклибинитиализе**](auxklibinitialize-func.md)
</dt> <dt>

[**\_ \_ основные \_ сведения о модуле AUX**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ Расширенная \_ информация о модуле AUX**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




