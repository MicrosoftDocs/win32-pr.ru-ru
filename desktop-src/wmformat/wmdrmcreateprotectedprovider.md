---
title: Функция Вмдрмкреатепротектедпровидер (Вмдрмсдк. h)
description: Функция Вмдрмкреатепротектедпровидер создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.
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
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694554"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Функция Вмдрмкреатепротектедпровидер

Функция **вмдрмкреатепротектедпровидер** создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media. Эта функция требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, поддерживающие защищенные функции DRM.

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



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции**](drm-functions.md)
</dt> <dt>

[**вмдрмкреатепровидер**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





