---
description: Включает фильтр обработки изображений для записи свойств обратно в драйвер (и на устройство).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Метод Ивиаимажефилтер:: Апплипропертиес (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711956"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>Метод Ивиаимажефилтер:: Апплипропертиес

Включает фильтр обработки изображений для записи свойств обратно в драйвер (и на устройство).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиапропертистораже* \[ окне\]
</dt> <dd>

Тип: **[**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

Указывает указатель на [_ *ивиапропертистораже* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для применяемых свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Не вызывайте этот метод непосредственно из приложения. Он вызывается функцией получения образа Windows (WIA) 2,0 после того, как фильтр обработки образов обработал необработанные данные.

*пвиапропертистораже* — это интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , в который фильтр обработки изображений должен записывать свойства. Фильтр обработки изображений должен использовать только метод [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) для записи свойств.

Этот метод позволяет фильтру обработки изображений записывать свойства обратно в драйвер (и на устройство). Это может потребоваться для фильтров, которые реализуют такие функции, как автоматическая раскрытие во время сканирования пленки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
