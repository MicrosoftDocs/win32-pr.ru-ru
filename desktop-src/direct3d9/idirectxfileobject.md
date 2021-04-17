---
description: Приложения используют методы интерфейса Идиректксфилеобжект для получения сведений о файловых объектах Microsoft DirectX. Не рекомендуется.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Интерфейс Идиректксфилеобжект (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684990"
---
# <a name="idirectxfileobject-interface"></a>Интерфейс Идиректксфилеобжект

Приложения используют методы интерфейса Идиректксфилеобжект для получения сведений о файловых объектах Microsoft DirectX. Не рекомендуется.

## <a name="members"></a>Элементы

Интерфейс **идиректксфилеобжект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Идиректксфилеобжект** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **идиректксфилеобжект** содержит следующие методы.



| Метод                                         | Описание                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Получает указатель на идентификатор GUID, определяющий объект файла DirectX. Не рекомендуется.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Получает указатель на имя объекта файла DirectX. Не рекомендуется.<br/>                   |



 

## <a name="remarks"></a>Комментарии

Идентификатор GUID для интерфейса Идиректксфилеобжект — IID \_ идиректксфилеобжект.

Тип ЛПДИРЕКТКСФИЛЕОБЖЕКТ определяется как указатель на этот интерфейс.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файловые интерфейсы X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
