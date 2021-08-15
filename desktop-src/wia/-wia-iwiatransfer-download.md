---
description: Инициирует загрузку данных в вызывающий объект.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: 'Ивиатрансфер: метод:D гружать (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 039b7dd4579419bac744a07bbc6ddd55c4b0b2e2e713340bf256fdb95d8fc071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450214"
---
# <a name="iwiatransferdownload-method"></a>Ивиатрансфер: метод:D гружать

Инициирует загрузку данных в вызывающий объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*пивиатрансферкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[ **ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md)\***

Указывает указатель на интерфейс [**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) вызывающего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

При скачивании папки также переносятся все дочерние элементы этой папки. Каждый элемент передается в отдельном потоке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 




