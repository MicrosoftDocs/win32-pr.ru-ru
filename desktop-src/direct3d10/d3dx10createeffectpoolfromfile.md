---
description: Создайте пул эффектов из файла эффектов.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Функция D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 500e0a72bc239b6c3f67011ed7abc0421f11cd8b9e4f67cbc86087e45027522d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753404"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a>Функция D3DX10CreateEffectPoolFromFile

Создайте пул эффектов из файла эффектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Имя файла действия. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Этот параметр может принимать значение **NULL**.

</dd> <dt>

*ппрофиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.

</dd> <dt>

*Хлслфлагс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).

</dd> <dt>

*Фксфлагс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.

</dd> <dt>

*ппумп* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)). Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.

</dd> <dt>

*ппеффектпул* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***

Адрес указателя на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).

</dd> <dt>

*пперрорс* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.

</dd> <dt>

*фресулт* \[ заполняет\]
</dt> <dd>

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Указатель на возвращаемое значение. Может иметь **значение NULL**. Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

В этом примере создается пул эффектов на основе воздействия, используемого в [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
