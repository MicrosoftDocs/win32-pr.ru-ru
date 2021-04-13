---
description: Создает объект данных. Не рекомендуется.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Метод Идиректксфилесавеобжект:: Креатедатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354673"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>Метод Идиректксфилесавеобжект:: Креатедатаобжект

Создает объект данных. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ргуидтемплате* \[ окне\]
</dt> <dd>

Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Идентификатор GUID, представляющий шаблон объекта данных.

</dd> <dt>

*szName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя объекта данных. Укажите **значение NULL** , если у объекта нет имени.

</dd> <dt>

*пгуид* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий объект данных. Укажите **значение NULL** , если у объекта нет идентификатора GUID.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Размер объекта данных в байтах.

</dd> <dt>

*пвдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий все данные необходимых элементов.

</dd> <dt>

*ппдатаобж* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***

Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий созданный объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе

## <a name="remarks"></a>Комментарии

Если эталонный объект данных будет ссылаться на объект данных, параметр szName или пгуид должен иметь значение, отличное от **null**.

Сохраните все шаблоны с помощью метода [**идиректксфилесавеобжект:: саветемплатес**](idirectxfilesaveobject--savetemplates.md) перед сохранением данных, созданных этим методом. Сохраните созданные данные с помощью метода [**идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md) .

Если необходимо сохранить необязательные данные, используйте метод [**идиректксфиледата:: адддатаобжект**](idirectxfiledata--adddataobject.md) после использования этого метода и перед использованием [**Идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md). Если у объекта есть дочерние объекты, добавьте их перед вызовом **идиректксфилесавеобжект:: SaveData**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилесавеобжект](idirectxfilesaveobject.md)
</dt> <dt>

[**Идиректксфиледата:: Адддатаобжект**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**Идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**Идиректксфилесавеобжект:: Саветемплатес**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
