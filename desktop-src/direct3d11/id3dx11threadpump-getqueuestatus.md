---
title: Метод ID3DX11ThreadPump Жеткуеуестатус (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Возвращает количество элементов в каждой из трех очередей в конвейере потока.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Метод Жеткуеуестатус Direct3D 11
- Метод Жеткуеуестатус Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Жеткуеуестатус
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986906"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>Метод ID3DX11ThreadPump:: Жеткуеуестатус

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Возвращает количество элементов в каждой из трех очередей в конвейере потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиокуеуе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Число элементов в очереди ввода-вывода.

</dd> <dt>

*ппроцесскуеуе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Число элементов в очереди процессов.

</dd> <dt>

*пдевицекуеуе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Число элементов в очереди устройства.

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

 

