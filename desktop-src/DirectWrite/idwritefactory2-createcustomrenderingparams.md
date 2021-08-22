---
title: IDWriteFactory2 Креатекустомрендерингпарамс, метод
description: Создает объект параметров отрисовки с указанными свойствами.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Непосредственная запись метода Креатекустомрендерингпарамс
- Прямая запись метода Креатекустомрендерингпарамс, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Креатекустомрендерингпарамс
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e85057c28e1ad969fe72711c86aab9657126c760ea3041a08bc5101877686a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071697"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Метод IDWriteFactory2:: Креатекустомрендерингпарамс

Создает объект параметров отрисовки с указанными свойствами.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*цвет* 
</dt> <dd>

Тип: **float**

Значение гаммы, используемое для гамма-коррекции, которое должно быть больше нуля и не может превышать 256.

</dd> <dt>

*енханцедконтраст* 
</dt> <dd>

Тип: **float**

Степень контрастности, ноль или больше.

</dd> <dt>

*грайскалинханцедконтраст* 
</dt> <dd>

Тип: **float**

Степень контрастности, ноль или больше.

</dd> <dt>

*клеартипелевел* 
</dt> <dd>

Тип: **float**

Степень уровня ClearType, от 0,0 f (без ClearType) до 1,0 f (Полная технология ClearType).

</dd> <dt>

*пикселжеометри* 
</dt> <dd>

Тип: **[ **дврите \_ пиксель \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Геометрия точки устройства.

</dd> <dt>

*рендерингмоде* 
</dt> <dd>

Тип: **[ **\_ \_ режим рендеринга дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Метод отрисовки глифов. В большинстве случаев это должен быть ДВРИТЕ \_ \_ режим рендеринга \_ по умолчанию для автоматического использования соответствующего режима.

</dd> <dt>

*гридфитмоде* 
</dt> <dd>

Тип: **[ **дврите \_ \_ \_ режим вписывания в сетку**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Как поместить контур глифа в сетку. В большинстве случаев это должно быть ДВРИТЕ \_ Сетка \_ \_ по умолчанию для автоматического выбора соответствующего режима.

</dd> <dt>

*рендерингпарамс* \[ заполняет\]
</dt> <dd>

Тип: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Содержит только что созданный объект параметров отрисовки или значение NULL в случае сбоя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

