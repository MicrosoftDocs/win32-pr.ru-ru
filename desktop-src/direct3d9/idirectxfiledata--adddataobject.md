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
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355400"
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

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода используйте метод [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект [**идиректксфиледата**](idirectxfiledata.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> <dt>

[**Идиректксфилесавеобжект:: Креатедатаобжект**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




