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
ms.openlocfilehash: 293525d570540e00da4e8ac7680cf850b253c7e3ccbe3ffd152b639d0bc139cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747274"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[идиректксфилесавеобжект](idirectxfilesaveobject.md)
</dt> </dl>

 

 




