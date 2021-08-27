---
title: Функция Вмдрмкреатепротектедпровидер (Вмдрмсдк. h)
description: функция вмдрмкреатепротектедпровидер создает фабрику класса, которая может создавать другие объекты расширенных api-интерфейсов клиента DRM Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Вмдрмкреатепротектедпровидер функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026932"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Функция Вмдрмкреатепротектедпровидер

функция **вмдрмкреатепротектедпровидер** создает фабрику класса, которая может создавать другие объекты расширенных api-интерфейсов клиента DRM Windows Media. Эта функция требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, поддерживающие защищенные функции DRM.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдрмпровидер* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**ивмдрмпровидер**](iwmdrmprovider.md) только что созданного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции**](drm-functions.md)
</dt> <dt>

[**вмдрмкреатепровидер**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





