---
title: 'Функция Texture2DMS:: Load (int, int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture2DMS:: Load (int, int, int, uint)'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352072"
---
# <a name="texture2dmsloadintintintuint-function"></a>Функция Texture2DMS:: Load (int, int, int, uint)

Считывает данные текстуры и возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **int2**

Координаты текстуры.

</dd> <dt>

*sampleindex* \[ окне\]
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Пример индекса.

</dd> <dt>

*Смещение* \[ окне\]
</dt> <dd>

Тип: **int2**

Смещение, применяемое к координатам текстуры перед загрузкой.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип:

Возвращаемый тип соответствует типу в объявлении для объекта [**Texture2DMS**](sm5-object-texture2dms.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
