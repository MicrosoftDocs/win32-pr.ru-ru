---
title: 'Функция Texture2DArray:: Load (int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture2DArray:: Load (int, int, uint)'
ms.assetid: 551EA931-6D24-478B-B741-3DD5B1E030E2
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
ms.openlocfilehash: 0907ddb4f5100ae6bffc81214ed0bed0d7857462e12c4625f179d6b769915569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723589"
---
# <a name="texture2darrayloadintintuint-function"></a>Функция Texture2DArray:: Load (int, int, uint)

Считывает данные текстуры и возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
 Load(
  in  int  Location,
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

Возвращаемый тип соответствует типу в объявлении для объекта [**Texture2DArray**](sm5-object-texture2darray.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](texture2darray-load.md)
</dt> </dl>

 

 
