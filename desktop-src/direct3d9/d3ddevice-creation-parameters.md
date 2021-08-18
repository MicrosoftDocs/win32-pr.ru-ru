---
description: Описывает параметры создания для устройства.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Структура D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805023"
---
# <a name="d3ddevice_creation_parameters-structure"></a>\_ \_ Структура параметров создания D3DDEVICE

Описывает параметры создания для устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Члены

<dl> <dt>

**адаптерординал**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Порядковый номер, обозначающий адаптер дисплея. D3DADAPTER \_ по умолчанию всегда является основным видеоадаптером. Используйте это порядковое числитель в качестве параметра адаптера для любого из методов [**IDirect3D9**](/windows/desktop/api) . Обратите внимание, что разные экземпляры объектов Direct3D 9,0 могут использовать разные порядковые номера. Адаптеры могут вводить или оставлять систему в том случае, если пользователи, например, добавляют или удаляют мониторы из системы с несколькими мониторами или при горячей замене ноутбука. Следовательно, используйте это порядковое имя только в экземпляре Direct3D 9,0, известном как допустимый, то есть в Direct3D 9,0, который создал этот интерфейс [**IDirect3DDevice9**](/windows/desktop/api) , или Direct3D 9,0, возвращенном из [**Direct3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), как вызвано через этот интерфейс **IDirect3DDevice9** .

</dd> <dt>

**DeviceType**
</dt> <dd>

Тип: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Член перечисляемого типа [**D3DDEVTYPE**](./d3ddevtype.md) . Обозначает количество эмулированных функций для этого устройства. Значение этого параметра отражает значение, передаваемое в вызов [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) , который создал это устройство.

</dd> <dt>

**хфокусвиндов**
</dt> <dd>

Тип: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Маркер окна, к которому относится фокус для этого устройства Direct3D. Значение этого параметра отражает значение, передаваемое в вызов [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) , который создал это устройство.

</dd> <dt>

**бехавиорфлагс**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Сочетание одной или нескольких констант [D3DCREATE](d3dcreate.md) , управляющих глобальным поведением устройства. Эти константы отражают константы, передаваемые в [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) при создании устройства.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**жеткреатионпараметерс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
