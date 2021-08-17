---
description: Объект обработки данных, используемый интерфейсом ID3DX10ThreadPump для асинхронной обработки загруженных данных.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Интерфейс ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128376"
---
# <a name="id3dx10dataprocessor-interface"></a>Интерфейс ID3DX10DataProcessor

Объект обработки данных, используемый [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для асинхронной обработки загруженных данных.

## <a name="members"></a>Элементы

Интерфейс **ID3DX10DataProcessor** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataProcessor** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10DataProcessor** содержит следующие методы.



| Метод                                                                | Описание                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**креатедевицеобжект**](id3dx10dataprocessor-createdeviceobject.md) | Создайте объект устройства.<br/>                                                                                                  |
| [**Уничтожить**](id3dx10dataprocessor-destroy.md)                       | Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для уничтожения процессора после завершения рабочего элемента.<br/> |
| [**Процесс**](id3dx10dataprocessor-process.md)                       | Обработка некоторых данных.<br/>                                                                                                       |



 

## <a name="remarks"></a>Remarks

Этот объект может быть унаследован и его члены переопределены. Это позволит настроить API для обработки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
