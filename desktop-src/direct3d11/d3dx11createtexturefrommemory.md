---
title: Функция D3DX11CreateTextureFromMemory (D3DX11. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать следующие библиотеки Директкстк (Runtime), Креатекскскстекстурефроммемори (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Затем Креатетекстуре создает ресурс текстуры из файла, находящегося в системной памяти.
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- D3DX11CreateTextureFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000442"
---
# <a name="d3dx11createtexturefrommemory-function"></a>Функция D3DX11CreateTextureFromMemory

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать следующие средства:
>
> -   Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОММЕМОРИ** (где XXX — DDS или WIC)
> -   Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСМЕМОРИ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатетекстуре**

 

Создайте ресурс текстуры из файла, находящегося в системной памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
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

Указатель на ресурс в системной памяти.

</dd> <dt>

*Сркдатасизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Размер ресурса в системной памяти.

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

*пптекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

Адрес указателя на созданный ресурс. См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

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
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

