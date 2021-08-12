---
description: Инициализирует фильтр. вызывается Windows получения образа (WIA) 2,0 перед загрузкой каждого образа.
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
ms.openlocfilehash: 43b818c3adc9926c4ba27f11f5d489ffc0b97e4443d0427e7a12067e9062072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440449"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Метод Ивиаимажефилтер:: Инитиализефилтер

Инициализирует фильтр. вызывается Windows получения образа (WIA) 2,0 перед загрузкой каждого образа.

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

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Указывает указатель на элемент [**IWiaItem2**](-wia-iwiaitem2.md) , представляющий изображение для предварительного просмотра.

</dd> <dt>

*пвиатрансферкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[ **ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md)\***

Указывает указатель на интерфейс [**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод вызывается, когда приложение вызывает [**загрузку**](-wia-iwiatransfer-download.md) и когда приложение вызывает функцию компонента предварительной версии WIA 2,0 `GetNewPreview` . **Ивиаимажефилтер:: инитиализефилтер** сохраняет ссылки на *pWiaItem2* и *пвиатрансферкаллбакк* для передачи в эти функции. Эти два указателя интерфейса должны храниться как переменные члена, и [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) следует вызывать для каждого из них. Указатели интерфейса также необходимы в реализации фильтра [**трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) и [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md) во время получения образа.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
