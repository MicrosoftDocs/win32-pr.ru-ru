---
description: Используется для установки и запроса эффектов, а также для выбора методов. Объект Effect может содержать несколько методов для визуализации одного и того же результата.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Интерфейс ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9f5bdcf90b3e0d317290a569984d1b72d248079de5b3b281325e66af6e443c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494024"
---
# <a name="id3dxeffect-interface"></a>Интерфейс ID3DXEffect

Используется для установки и запроса эффектов, а также для выбора методов. Объект Effect может содержать несколько методов для визуализации одного и того же результата.

## <a name="members"></a>Элементы

Интерфейс **ID3DXEffect** наследует от [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXEffect** содержит следующие методы.



| Метод                                                                | Описание                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**апплипараметерблокк**](id3dxeffect--applyparameterblock.md)       | Применить значения в блоке состояния к текущему состоянию системы.<br/>                                                                                                                 |
| [**Начать**](id3dxeffect--begin.md)                                   | Запускает активный метод.<br/>                                                                                                                                                           |
| [**бегинпараметерблокк**](id3dxeffect--beginparameterblock.md)       | Начать запись изменений состояния в блоке параметров.<br/>                                                                                                                                   |
| [**бегинпасс**](id3dxeffect--beginpass.md)                           | Начинает проход в активном методе.<br/>                                                                                                                                           |
| [**клониффект**](id3dxeffect--cloneeffect.md)                       | Создает копию результата.<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.<br/>                                                                                           |
| [**делетепараметерблокк**](id3dxeffect--deleteparameterblock.md)     | Удаляет блок параметров.<br/>                                                                                                                                                             |
| [**Конец**](id3dxeffect--end.md)                                       | Завершает активный метод.<br/>                                                                                                                                                             |
| [**ендпараметерблокк**](id3dxeffect--endparameterblock.md)           | Прерывать изменения состояния параметров эффектов записи.<br/>                                                                                                                                        |
| [**ендпасс**](id3dxeffect--endpass.md)                               | Завершение активного прохода.<br/>                                                                                                                                                                   |
| [**финднекствалидтечникуе**](id3dxeffect--findnextvalidtechnique.md) | Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.<br/>                                                                                       |
| [**жеткурренттечникуе**](id3dxeffect--getcurrenttechnique.md)       | Возвращает текущий метод.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Извлекает устройство, связанное с этим действием.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Возвращает указатель на пул общих параметров.<br/>                                                                                                                                      |
| [**жетстатеманажер**](id3dxeffect--getstatemanager.md)               | Получение диспетчера состояний эффектов.<br/>                                                                                                                                                         |
| [**испараметерусед**](id3dxeffect--isparameterused.md)               | Определяет, используется ли параметр методом.<br/>                                                                                                                                   |
| [**онлостдевице**](id3dxeffect--onlostdevice.md)                     | Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.<br/> |
| [**онресетдевице**](id3dxeffect--onresetdevice.md)                   | Этот метод используется для повторного получения ресурсов и сохранения начального состояния.<br/>                                                                                                                       |
| [**сетраввалуе**](id3dxeffect--setrawvalue.md)                       | Установка непрерывного диапазона констант шейдера с копированием в памяти.<br/>                                                                                                                        |
| [**сетстатеманажер**](id3dxeffect--setstatemanager.md)               | Задайте диспетчер состояний эффектов.<br/>                                                                                                                                                         |
| [**сеттечникуе**](id3dxeffect--settechnique.md)                     | Задает активный метод.<br/>                                                                                                                                                            |
| [**валидатетечникуе**](id3dxeffect--validatetechnique.md)           | Проверка метода.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarks

Интерфейс ID3DXEffect получается путем вызова [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)или [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).

Тип LPD3DXEFFECT определяется как указатель на этот интерфейс.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




