---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DDisassemble. Эта функция, которая разбивает скомпилированный результат на текстовую строку, содержащую инструкции ассемблера и назначения регистров, является устаревшей.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Функция D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 282dcbb91013e5e8bf6def540809fa3afdb3bca40e2a2fd5250c5b3c92877af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753284"
---
# <a name="d3dx10disassembleeffect-function"></a>Функция D3DX10DisassembleEffect

> [!Note]  
> Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

Эта функция, которая разбивает скомпилированный результат на текстовую строку, содержащую инструкции ассемблера и назначения регистров, является устаревшей. Вместо этого используйте [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пеффект* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Указатель на интерфейс Effect (см. [**интерфейс ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*Енаблеколоркоде* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Включить HTML-теги в выходные данные, чтобы получить цветовой код для результата.

</dd> <dt>

*ппдисассембли* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Адрес буфера (см. [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит разсобранный результат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
