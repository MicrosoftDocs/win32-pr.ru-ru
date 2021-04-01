---
title: IMsRdpClientAdvancedSettings7 Суперпанакцелератионфактор, свойство
description: Указывает или получает значение, указывающее коэффициент ускорения Суперпан. Коэффициент ускорения Суперпан определяет скорость движения экрана в режиме Суперпан.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Суперпанакцелератионфактор
- Службы удаленных рабочих столов свойства Суперпанакцелератионфактор, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Суперпанакцелератионфактор
- Службы удаленных рабочих столов свойства Суперпанакцелератионфактор, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Суперпанакцелератионфактор
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989414"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Суперпанакцелератионфактор

Указывает или получает значение, указывающее коэффициент ускорения Суперпан. Коэффициент ускорения Суперпан определяет скорость движения экрана в режиме Суперпан. Коэффициент ускорения — это число пикселей, которое прокручивается на экране в заданном направлении для каждого пикселя движения мыши клиентом.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Значение свойства

Устанавливаемый коэффициент ускорения Суперпан. Коэффициент ускорения Суперпан — это число пикселей, которое экранное представление прокручивается в заданном направлении для каждого пикселя движения мыши.

## <a name="remarks"></a>Комментарии

Дополнительные сведения о Суперпан см. в разделе [**енаблесуперпан**](imsrdpclientadvancedsettings7-enablesuperpan.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**енаблесуперпан**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





