---
title: Функция D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки. Создайте обработчик данных, который будет использоваться в конвейере потоков. | Функция D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- D3DX11CreateAsyncTextureInfoProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da992c258fe79bd1ed81274495e884339f40aed337fcf11665ec27110afaf422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536263"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a>Функция D3DX11CreateAsyncTextureInfoProcessor

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки.

 

Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx11threadpump.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пимажеинфо* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***

Необязательный элемент. Определяет характеристики текстуры (см. [**\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.

</dd> <dt>

*ппдатапроцессор* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот API создает интерфейс процессора данных; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) создает интерфейс процессора данных и загружает текстуру.

Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.

для приложений магазина Windows, примеры DirectX (например, [пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , использующий среда выполнения Windows асинхронной модели программирования ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

для классических приложений Win32 можно использовать [среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

