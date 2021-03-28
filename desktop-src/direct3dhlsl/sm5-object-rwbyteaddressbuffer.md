---
title: рвбитеаддрессбуффер
description: Буфер чтения/записи, в котором индексы в байтах.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- Рвбитеаддрессбуффер HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412990"
---
# <a name="rwbyteaddressbuffer"></a>рвбитеаддрессбуффер

Буфер чтения/записи, в котором индексы в байтах.



| Метод                                                                                          | Описание                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Возвращает размеры ресурсов.       |
| [**интерлоккедадд**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Атомарно добавляет,                   |
| [**интерлоккеданд**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | And, атомарно.                   |
| [**интерлоккедкомпариксчанже**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Сравнение и обмен атомарно. |
| [**интерлоккедкомпаресторе**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Сравнивает и сохраняет атомарно.    |
| [**интерлоккедексчанже**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Exchange, атомарно.              |
| [**интерлоккедмакс**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Выполняет поиск максимального, атомарного.          |
| [**интерлоккедмин**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Найти минимальное и атомарное значение.           |
| [**Взаимоблокировка**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | OR, атомарно.                    |
| [**интерлоккедксор**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | Ксорс, атомарно.                   |
| [**Загрузить**](rwbyteaddressbuffer-load.md)                                                        | Возвращает одно значение.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Возвращает два значения.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Возвращает три значения.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Возвращает четыре значения.                   |
| [**Магазин**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Задает одно значение.                     |
| [**Store2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Задает два значения.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Задает три значения.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Задает четыре значения.                   |



 

Для объектов Рвбитеаддрессбуффер можно использовать префикс класса хранения **глобалликохерент**. Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи. Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.

Формат UAV, привязанный к этому ресурсу, должен быть создан в формате DXGI \_ \_ R32 без \_ типа.

UAV, привязанный к этому ресурсу, должен быть создан с помощью [**D3D11 \_ buffer \_ UAV \_ флаг \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Тип объекта **рвбитеаддрессбуффер** можно использовать при работе с необработанными буферами. Дополнительные сведения об исходном просмотре буферов см. в разделе [необработанные представления буферов](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот объект поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Поддерживается |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Модель](d3d11-graphics-reference-sm5.md) шейдера модели построителя текстуры 5 и более поздних моделей [построителя текстуры 4](dx-graphics-hlsl-sm4.md) (доступна через API Direct3D 11 с использованием уровня компонентов 10,0 или 10,1 ([**\_ \_ уровень компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) на устройствах, поддерживающих шейдеры вычислений. Дополнительные сведения о поддержке COMPUTE Shader на оборудовании нижнего уровня см. в разделе Вычисление шейдеров на несущем [оборудовании](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | да       |



 

Этот объект поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

