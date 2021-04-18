---
description: Подготавливает устройство для рисования спрайтов.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Метод ID3DXSprite:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713771"
---
# <a name="id3dxspritebegin-method"></a>Метод ID3DXSprite:: Begin

Подготавливает устройство для рисования спрайтов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов, описывающих параметры визуализации спрайта. Для этого метода допустимы следующие флаги:

-   D3DXSPRITE \_ алфабленд
-   D3DXSPRITEный \_ \_ стенд
-   D3DXSPRITE \_ донотмодифи \_ рендерстате
-   D3DXSPRITE \_ донотсавестате
-   D3DXSPRITE \_ обжектспаце
-   D3DXSPRITE \_ \_ Сортировка \_ глубины \_ бакктофронт
-   D3DXSPRITE \_ \_ Сортировка \_ глубины \_ фронттобакк
-   \_ \_ \_ ТЕКСТУРа сортировки D3DXSPRITE

Описание флагов и сведения о том, как управлять записью состояния устройства и преобразованиями представлений устройств, см. в разделе [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Этот метод должен вызываться из [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) . . . Последовательность [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) . **ID3DXSprite:: Begin** не может использоваться в качестве замены для **IDirect3DDevice9:: бегинсцене** или [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md).

Этот метод настроит следующие состояния на устройстве.

Состояния рендеринга:



| Тип ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Значение                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ алфабленденабле                                       | true                                                                                                              |
| D3DRS \_ алфафунк                                              | D3DCMP \_                                                                                                   |
| D3DRS \_ алфареф                                               | 0x00                                                                                                              |
| D3DRS \_ алфатестенабле                                        | алфакмпкапс                                                                                                      |
| D3DRS \_ блендоп                                                | D3DBLENDOP \_ Добавить                                                                                                   |
| D3DRS \_ Обрезка                                               | true                                                                                                              |
| D3DRS \_ клиппланинабле                                        | FALSE                                                                                                             |
| D3DRS \_ колорвритинабле                                       | D3DCOLORWRITEENABLE \_ альфа \| D3DCOLORWRITEENABLE \_ Blue \| D3DCOLORWRITEENABLE \_ зеленый \| D3DCOLORWRITEENABLE \_ красный |
| D3DRS \_ куллмоде                                               | D3DCULL \_ None                                                                                                     |
| D3DRS \_ дестбленд                                              | D3DBLEND \_ инвсркалфа                                                                                             |
| D3DRS \_ диффусематериалсаурце                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ енаблеадаптиветесселлатион                             | FALSE                                                                                                             |
| D3DRS \_ филлмоде                                               | D3DFILL \_                                                                                                    |
| D3DRS \_ фоженабле                                              | FALSE                                                                                                             |
| D3DRS \_ индекседвертексбленденабле                               | FALSE                                                                                                             |
| \_Освещение D3DRS                                               | FALSE                                                                                                             |
| D3DRS \_ ранжефоженабле                                         | FALSE                                                                                                             |
| D3DRS \_ сепаратеалфабленденабле                               | FALSE                                                                                                             |
| D3DRS \_ шадемоде                                              | D3DSHADE метод \_ Гуро                                                                                                 |
| D3DRS \_ спекуларенабле                                         | FALSE                                                                                                             |
| D3DRS \_ сркбленд                                               | D3DBLEND \_ сркалфа                                                                                                |
| D3DRS \_ сргбвритинабле                                        | FALSE                                                                                                             |
| D3DRS \_ стенЦиленабле                                          | FALSE                                                                                                             |
| D3DRS \_ вертексбленд                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Состояние этапа текстуры:



| Идентификатор этапа | Тип ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Значение            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | \_Текстура D3DTA   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ диффузный   |
| 0                | D3DTSS \_ алфаоп                                                           | D3DTOPная \_ модуляция |
| 0                | D3DTSS \_ COLORARG1                                                         | \_Текстура D3DTA   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ диффузный   |
| 0                | D3DTSS \_ колороп                                                           | D3DTOPная \_ модуляция |
| 0                | D3DTSS \_ текскурдиндекс                                                     | 0                |
| 0                | D3DTSS \_ текстуретрансформфлагс                                             | \_Отключение D3DTTFF |
| 1                | D3DTSS \_ алфаоп                                                           | \_Отключение D3DTOP  |
| 1                | D3DTSS \_ колороп                                                           | \_Отключение D3DTOP  |



 

Состояния образцов:



| Индекс этапа образца | Тип ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Значение                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ аддрессу                                               | D3DTADDRESSный \_ срез                                                                                             |
| 0                   | D3DSAMP \_ аддрессв                                               | D3DTADDRESSный \_ срез                                                                                             |
| 0                   | D3DSAMP \_ магфилтер                                              | D3DTEXF \_ анизотроп, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ магфанисотропик; в противном случае — \_ линейное D3DTEXF |
| 0                   | D3DSAMP \_ максмиплевел                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ максанисотропи                                          | максанисотропи                                                                                                  |
| 0                   | D3DSAMP \_ минфилтер                                              | D3DTEXF \_ анизотроп, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ минфанисотропик; в противном случае — \_ линейное D3DTEXF |
| 0                   | D3DSAMP \_ мипфилтер                                              | D3DTEXF \_ линейный, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ мипфлинеар; в противном случае D3DTEXF \_ Point            |
| 0                   | D3DSAMP \_ мипмаплодбиас                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ сргбтекстуре                                            | 0                                                                                                              |



 

> [!Note]  
> Этот метод отключает N-патчи.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
