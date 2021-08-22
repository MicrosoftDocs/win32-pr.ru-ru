---
description: Проверяет параметры создания текстуры.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Функция D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c7166f981c0351054a2a6c359127a4ce1959b45a6e71c44db9e2546825bc5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496104"
---
# <a name="d3dxchecktexturerequirements-function"></a>Функция D3DXCheckTextureRequirements

Проверяет параметры создания текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.

</dd> <dt>

*пвидс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на запрошенную ширину в пикселях или **значение NULL**. Возвращает исправленный размер.

</dd> <dt>

*феигхт* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на запрошенную высоту в пикселях или **значение NULL**. Возвращает исправленный размер.

</dd> <dt>

*пнуммиплевелс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на число запрошенных уровней mipmap или **значение NULL**. Возвращает исправленное число уровней mipmap.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

0 или [**D3DUSAGE \_ рендертаржет**](d3dusage.md). Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга. Затем ресурс можно передать в параметр Пневрендертаржет метода [**сетрендертаржет**](/windows/desktop/api) . Если указан параметр **D3DUSAGE \_ рендертаржет** , приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*пформат* \[ в, out\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)\***

Указатель на член перечисляемого типа [D3DFORMAT](d3dformat.md) . Указывает требуемый формат пикселей или **значение NULL**. Возвращает исправленный формат.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Remarks

Если параметры для этой функции недопустимы, эта функция возвращает исправленные параметры.

Эта функция использует следующие эвристики при сравнении запрошенных требований с доступными форматами:

-   Не выбирайте формат с меньшим числом каналов.
-   Избегайте использования типов [FourCC](d3dformat.md) и 24-разрядных форматов, если они не запрошены явным образом.
-   Попробуйте не добавлять новые каналы.
-   Попробуйте не изменять число бит на канал.
-   Старайтесь не преобразовывать типы форматов. Например, Избегайте преобразования формата ARGB в формат глубины.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
