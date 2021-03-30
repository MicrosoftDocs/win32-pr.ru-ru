---
description: Сохраняет шаблоны в файл DirectX. Не рекомендуется.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Метод Идиректксфилесавеобжект:: Саветемплатес (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354670"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Метод Идиректксфилесавеобжект:: Саветемплатес

Сохраняет шаблоны в файл DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ктемплатес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Общее число шаблонов для сохранения.

</dd> <dt>

*ппгуидтемплатес* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \* \***

Адрес указателя на массив идентификаторов GUID для всех шаблонов, которые необходимо сохранить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.

## <a name="remarks"></a>Комментарии

В следующем фрагменте кода приведен пример вызова **идиректксфилесавеобжект:: саветемплатес** и примера содержимого для массива, в который указывает ппгуидтемплатес.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



После использования этого метода для сохранения шаблонов используйте метод [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилесавеобжект](idirectxfilesaveobject.md)
</dt> <dt>

[**Идиректксфилесавеобжект:: Креатедатаобжект**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
