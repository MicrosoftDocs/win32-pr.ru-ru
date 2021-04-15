---
title: Функция Жетрекуирединтермедиатесизе (D3dx12. h)
description: Возвращает требуемый размер буфера, используемый для передачи данных.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Функция Жетрекуирединтермедиатесизе
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647863"
---
# <a name="getrequiredintermediatesize-function"></a>Функция Жетрекуирединтермедиатесизе

Возвращает требуемый размер буфера, используемый для передачи данных.

## <a name="syntax"></a>Синтаксис


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестинатионресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий целевой ресурс.

</dd> <dt>

*Фирстсубресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс первого подресурса в ресурсе. Диапазон допустимых значений — от 0 до D3D12 \_ требований к \_ подресурсам.

</dd> <dt>

*Нумсубресаурцес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число подресурсов в ресурсе. Диапазон допустимых значений — от 0 до (D3D12 \_ req \_ Resources- *фирстсубресаурце*).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Размер буфера в байтах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

