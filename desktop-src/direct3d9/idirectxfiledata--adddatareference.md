---
description: Создает и добавляет объект ссылки на данные в качестве дочернего объекта. Не рекомендуется.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Метод Идиректксфиледата:: Адддатареференце (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713629"
---
# <a name="idirectxfiledataadddatareference-method"></a>Метод Идиректксфиледата:: Адддатареференце

Создает и добавляет объект ссылки на данные в качестве дочернего объекта. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сзреф* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя объекта данных, на который указывает ссылка. Этот параметр может иметь **значение NULL** , если пгуидреф предоставляет ссылку на идентификатор GUID.

</dd> <dt>

*пгуидреф* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий данные. Этот параметр может иметь **значение NULL** , если сзреф предоставляет ссылку на имя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе

## <a name="remarks"></a>Комментарии

Чтобы этот метод был выполнен, параметр Сзреф или Пгуидреф должен иметь значение, отличное от **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> </dl>

 

 
