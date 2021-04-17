---
description: Добавьте рабочий элемент в конвейер потоков.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'Метод ID3DX10ThreadPump:: Аддворкитем (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704016"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>Метод ID3DX10ThreadPump:: Аддворкитем

Добавьте рабочий элемент в конвейер потоков.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдаталоадер* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Загрузчик, который будет использоваться генератором потоков, когда для рабочего элемента требуется загрузка данных.

</dd> <dt>

*пдатапроцессор* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

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

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




