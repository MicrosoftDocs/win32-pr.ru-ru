---
description: Определяет типы устройств.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Перечисление D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694118"
---
# <a name="d3ddevtype-enumeration"></a>Перечисление D3DDEVTYPE

Определяет типы устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**
</dt> <dd>

Аппаратное растрирование. Заливка выполняется программным обеспечением, оборудованием, смешанным преобразованием и освещением.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ нуллреф**
</dt> <dd>

Инициализируйте Direct3D на компьютере, на котором нет доступных растровых устройств и ссылок на них, и включите ресурсы для создания трехмерного содержимого. См. заметки.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**
</dt> <dd>

Функции Direct3D реализуются в программном обеспечении. Однако в этом случае средство программной прорисовки использует специальные инструкции ЦП, когда это возможно.

Эталонное устройство устанавливается Windows SDK 8,0 или более поздней версии и предназначено для помощи в отладке только для разработки.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Подключаемое программное устройство, зарегистрированное с помощью [**IDirect3D9:: регистерсофтваредевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Все методы интерфейса [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) , которые принимают тип устройства **D3DDEVTYPE** , завершатся ошибкой, если \_ задано D3DDEVTYPE нуллреф. Чтобы использовать эти методы, замените D3DDEVTYPE \_ ref в вызове метода.

Устройство D3DDEVTYPE \_ ref должно быть создано в памяти с \_ рабочей областью D3DPOOL, если только не требуются буферы вершин и индексов. Для поддержки буферов вершин и индексов Создайте устройство в памяти D3DPOOL \_ системмем.

Если установлен D3dref9.dll, Direct3D будет использовать средство программной прорисовки для создания \_ типа устройства D3DDEVTYPE, даже если \_ задано D3DDEVTYPE нуллреф. Если D3dref9.dll недоступен и указан параметр D3DDEVTYPE \_ нуллреф, то Direct3D не будет ни визуализировать сцену, ни представлять ее.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9:: Чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9:: Чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9:: Чеккдевицетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9:: Креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9:: Жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_Параметры создания \_ D3DDEVICE**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
