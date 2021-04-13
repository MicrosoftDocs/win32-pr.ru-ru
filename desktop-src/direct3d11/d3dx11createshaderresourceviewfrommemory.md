---
title: Функция D3DX11CreateShaderResourceViewFromMemory (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать следующие библиотеки Директкстк (Runtime), Креатекскскстекстурефроммемори (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Затем Креатешадерресаурцевиев создать представление шейдера-ресурсов из файла в памяти.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- D3DX11CreateShaderResourceViewFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0730fafdeb85cc22944f282eaaf556a1cdb12d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998522"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a>Функция D3DX11CreateShaderResourceViewFromMemory

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать следующие средства:
>
> -   Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОММЕМОРИ** (где XXX — DDS или WIC)
> -   Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСМЕМОРИ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатешадерресаурцевиев**

 

Создание представления "шейдер — представление ресурсов" из файла в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Указатель на устройство (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использовать ресурс.

</dd> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**

Указатель на файл в памяти, который содержит представление "шейдер-ресурс".

</dd> <dt>

*Сркдатасизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Размер файла в памяти.

</dd> <dt>

*плоадинфо* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***

Необязательный параметр. Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.

</dd> <dt>

*ппумп* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)). Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.

</dd> <dt>

*ппшадерресаурцевиев* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Адрес указателя на только что созданное представление ресурсов шейдера. См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> <dt>

*фресулт* \[ заполняет\]
</dt> <dd>

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Указатель на возвращаемое значение. Может иметь **значение NULL**. Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

