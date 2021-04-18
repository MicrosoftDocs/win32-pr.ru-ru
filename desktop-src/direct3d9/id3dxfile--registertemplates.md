---
description: Регистрирует пользовательские шаблоны.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'Метод ID3DXFile:: Регистертемплатес (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713778"
---
# <a name="id3dxfileregistertemplates-method"></a>Метод ID3DXFile:: Регистертемплатес

Регистрирует пользовательские шаблоны.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на буфер, состоящий из файла. x в текстовом или двоичном формате, содержащем шаблоны.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

Размер буфера, на который указывает Пвдата, в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.

## <a name="remarks"></a>Комментарии

В следующем фрагменте кода приведен пример вызова **регистертемплатес** и пример содержимого для буфера, на который указывает **пвдата** .


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



Все шаблоны должны указывать имя и UUID.

Этот метод вызывает метод [**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) , получая указатель интерфейса [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , вызывая [**креатинумобжект**](id3dxfile--createenumobject.md) с **пвдата** в качестве первого параметра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
