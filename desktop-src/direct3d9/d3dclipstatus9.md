---
description: Описывает текущее состояние отсечения.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Структура D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713575"
---
# <a name="d3dclipstatus9-structure"></a>Структура D3DCLIPSTATUS9

Описывает текущее состояние отсечения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Члены

<dl> <dt>

**клипунион**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Флаги объединения клипов, описывающие текущее состояние отсечения. Этот элемент может иметь один или несколько следующих флагов:



| Значение                                                                                                                                                      | Значение                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ все**</dt> </dl>          | Сочетание всех флагов клипа.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ слева**</dt> </dl>       | Все вершины обрезаются левой плоскостью просмотра фрустум.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ вправо**</dt> </dl>    | Все вершины обрезаются правой плоскостью просмотра фрустум.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ сверху**</dt> </dl>          | Все вершины обрезаются верхней плоскостью фрустум просмотра.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ снизу**</dt> </dl> | Все вершины обрезаются нижней плоскостью фрустум просмотра.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ спереди**</dt> </dl>    | Все вершины обрезаются передней плоскостью просмотра фрустум.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ назад**</dt> </dl>       | Все вершины обрезаются на задней плоскости фрустум просмотра.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Определяемые приложением отрезкиные плоскости.<br/>                                 |



 

</dd> <dt>

**клипинтерсектион**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Флаги пересечения фрагментов клипов, описывающие текущее состояние отсечения. Этот элемент может принимать те же флаги, что и Клипунион.

</dd> </dl>

## <a name="remarks"></a>Комментарии

При включении обрезки во время обработки вершин (с помощью [**процессвертицес**](/windows/desktop/api), [**дравпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)или других функций рисования) Direct3D вычислит код обрезки для каждой вершины. Фрагмент кода обрезки представляет собой сочетание \_ \* битов D3DCS. Если вершина находится за пределами определенной плоскости обрезки, соответствующий бит задается в коде обрезки. Direct3D поддерживает состояние отсечения с помощью **D3DCLIPSTATUS9**, который содержит элементы Клипунион и клипинтерсектион. Клипунион — это побитовое или из всех кодов зажимов вершин, а Клипинтерсектион — это побитовое и из всех кодов фрагментов вершин. Начальные значения для Клипунион и 0xFFFFFFFF для Клипинтерсектион равны нулю. Если \_ для D3DRS обрезки задано **значение false**, то для клипунион и клипинтерсектион устанавливается нулевое значение. Direct3D обновляет состояние отсечения во время вызовов рисования. Чтобы вычислить состояние отсечения для определенного объекта, задайте для Клипунион и Клипинтерсектион начальное значение и продолжайте рисование.

Состояние обрезки не обновляется [**дравректпатч**](/windows/desktop/api) и [**дравтрипатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) , так как для них отсутствует Эмуляция программного обеспечения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**жетклипстатус**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**сетклипстатус**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
