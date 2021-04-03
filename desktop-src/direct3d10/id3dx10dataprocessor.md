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
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914831"
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
| [**Завершить**](id3dx10dataprocessor-destroy.md)                       | Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для уничтожения процессора после завершения рабочего элемента.<br/> |
| [**Процесс**](id3dx10dataprocessor-process.md)                       | Обработка некоторых данных.<br/>                                                                                                       |



 

## <a name="remarks"></a>Комментарии

Этот объект может быть унаследован и его члены переопределены. Это позволит настроить API для обработки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
