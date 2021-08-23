---
description: Добавляет объект данных в качестве дочернего объекта. Не рекомендуется.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Метод Идиректксфиледата:: Адддатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491834"
---
# <a name="idirectxfiledataadddataobject-method"></a>Метод Идиректксфиледата:: Адддатаобжект

Добавляет объект данных в качестве дочернего объекта. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдатаобж* \[ окне\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)**

Указатель на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий файл данных файла, который необходимо добавить в качестве дочернего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе

## <a name="remarks"></a>Remarks

Перед вызовом этого метода используйте метод [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект [**идиректксфиледата**](idirectxfiledata.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> <dt>

[**Идиректксфилесавеобжект:: Креатедатаобжект**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




