---
description: Объект загрузки данных, используемый интерфейсом ID3DX10ThreadPump для асинхронной загрузки данных.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Интерфейс ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128366"
---
# <a name="id3dx10dataloader-interface"></a>Интерфейс ID3DX10DataLoader

Объект загрузки данных, используемый [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для асинхронной загрузки данных.

## <a name="members"></a>Элементы

Интерфейс **ID3DX10DataLoader** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataLoader** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10DataLoader** содержит следующие методы.



| Метод                                             | Описание                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Распаковки**](id3dx10dataloader-decompress.md) | Используется для распаковки закодированных данных. Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы. При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.<br/> |
| [**Уничтожить**](id3dx10dataloader-destroy.md)       | Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для уничтожения загрузчика после завершения рабочего элемента.<br/>                                                                                                   |
| [**Загрузить**](id3dx10dataloader-load.md)             | Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для загрузки данных с диска.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Remarks

Этот объект может быть унаследован и его члены переопределены. Это позволит вам настроить API для загрузки и распаковки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
