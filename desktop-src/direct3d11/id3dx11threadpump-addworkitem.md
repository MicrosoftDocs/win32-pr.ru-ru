---
title: Метод ID3DX11ThreadPump Аддворкитем (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Добавляет рабочий элемент в конвейер потока.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Метод Аддворкитем Direct3D 11
- Метод Аддворкитем Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Аддворкитем
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354273"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>Метод ID3DX11ThreadPump:: Аддворкитем

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Добавляет рабочий элемент в конвейер потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдаталоадер* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***

Загрузчик, который будет использоваться генератором потоков, когда для рабочего элемента требуется загрузка данных.

</dd> <dt>

*пдатапроцессор* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***

Процессор, который будет использоваться генератором потоков, когда для рабочего элемента требуются данные для обработки.

</dd> <dt>

*фресулт* \[ окне\]
</dt> <dd>

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Указатель на возвращаемое значение. Может иметь **значение NULL**.

</dd> <dt>

*ппдевицеобжект* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Устройство, использующее объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





