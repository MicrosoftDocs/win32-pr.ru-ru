---
title: 'Функция Texture2DMSArray:: Load (int, int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture2DMSArray:: Load (int, int, int, uint)'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c237de43a52650af1d365a6b95c47f51f525b698152b0be0adf2ffe83f15c1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506887"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a>Функция Texture2DMSArray:: Load (int, int, int, uint)

Считывает данные текстуры и возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **int**

Координаты текстуры.

</dd> <dt>

*sampleindex* \[ окне\]
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Пример индекса.

</dd> <dt>

*Смещение* \[ окне\]
</dt> <dd>

Тип: **int**

Смещение, применяемое к координатам текстуры перед выборкой.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип:

Возвращаемый тип соответствует типу в объявлении для объекта [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](texture2dmsarray-load.md)
</dt> <dt>

[**Texture2DMSArray**](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
