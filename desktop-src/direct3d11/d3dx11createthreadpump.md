---
title: Функция D3DX11CreateThreadPump (D3DX11core. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки. Создание конвейера потока.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3a19c338b330604caae9ce5a1e7f7222664b0521f9874c3eff07ff1fc8a4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536105"
---
# <a name="d3dx11createthreadpump-function"></a>Функция D3DX11CreateThreadPump

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки.

 

Создание конвейера потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Циосреадс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число потоков ввода-вывода для создания. Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.

</dd> <dt>

*кпроксреадс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число создаваемых потоков процесса. Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.

</dd> <dt>

*ппсреадпумп* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

Созданный конвейер потока. См. раздел [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Конвейер потоков — это очень ресурсоемкий объект. Для каждого приложения должен быть создан только один конвейер потока.

Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.

для приложений магазина Windows, примеры DirectX (например, [пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , использующий среда выполнения Windows асинхронной модели программирования ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

для классических приложений Win32 можно использовать [среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

