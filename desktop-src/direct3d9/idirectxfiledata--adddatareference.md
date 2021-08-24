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
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747264"
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

## <a name="remarks"></a>Remarks

Чтобы этот метод был выполнен, параметр Сзреф или Пгуидреф должен иметь значение, отличное от **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> </dl>

 

 
