---
description: Сохраняет объект данных и его дочерние элементы в файле DirectX. Не рекомендуется.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Метод Идиректксфилесавеобжект:: SaveData (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713626"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>Метод Идиректксфилесавеобжект:: SaveData

Сохраняет объект данных и его дочерние элементы в файле DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдатаобж* \[ окне\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)**

Указатель на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий объект данных файла для сохранения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаррайсизе, дксфилирр \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилесавеобжект](idirectxfilesaveobject.md)
</dt> </dl>

 

 




