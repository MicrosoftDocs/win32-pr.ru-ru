---
description: Инициализирует фильтр. Вызывается функцией получения образа Windows (WIA) 2,0 перед загрузкой каждого образа.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Метод Ивиаимажефилтер:: Инитиализефилтер (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711957"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Метод Ивиаимажефилтер:: Инитиализефилтер

Инициализирует фильтр. Вызывается функцией получения образа Windows (WIA) 2,0 перед загрузкой каждого образа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pWiaItem2* \[ окне\]
</dt> <dd>

Тип: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Указывает указатель на элемент [_ *IWiaItem2* *](-wia-iwiaitem2.md) , представляющий изображение для предварительного просмотра.

</dd> <dt>

*пвиатрансферкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _

Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* *](-wia-iwiatransfercallback.md) приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод вызывается, когда приложение вызывает [**загрузку**](-wia-iwiatransfer-download.md) и когда приложение вызывает функцию компонента предварительной версии WIA 2,0 `GetNewPreview` . **Ивиаимажефилтер:: инитиализефилтер** сохраняет ссылки на *pWiaItem2* и *пвиатрансферкаллбакк* для передачи в эти функции. Эти два указателя интерфейса должны храниться как переменные члена, и [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) следует вызывать для каждого из них. Указатели интерфейса также необходимы в реализации фильтра [**трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) и [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md) во время получения образа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
