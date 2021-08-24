---
description: Создание представления "шейдер — представление ресурсов" из файла.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: Функция D3DX10CreateShaderResourceViewFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 47c563a7a786dd78fab0ab7ee24e8b5fd535a6ea13b161b303bb1fda14693aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634674"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a>Функция D3DX10CreateShaderResourceViewFromFile

Создание представления "шейдер — представление ресурсов" из файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.

</dd> <dt>

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Имя файла, содержащего представление шейдера-ресурса. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> <dt>

*плоадинфо* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***

Необязательный элемент. Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.

</dd> <dt>

*ппумп* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Указатель на интерфейс генератора потоков (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)). Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.

</dd> <dt>

*ппшадерресаурцевиев* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Адрес указателя на представление шейдера-ресурса (см. [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).

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

Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
