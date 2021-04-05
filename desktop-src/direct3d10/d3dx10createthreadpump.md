---
description: Создание конвейера потока.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Функция D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000483"
---
# <a name="d3dx10createthreadpump-function"></a>Функция D3DX10CreateThreadPump

Создание конвейера потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Циосреадс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число потоков ввода-вывода для создания. Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.

</dd> <dt>

*кпроксреадс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число создаваемых потоков процесса. Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.

</dd> <dt>

*ппсреадпумп* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

Созданный конвейер потока. См. раздел [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Конвейер потоков — это очень ресурсоемкий объект. Для каждого приложения должен быть создан только один конвейер потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
