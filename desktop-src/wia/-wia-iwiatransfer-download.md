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
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541967"
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

Тип: **[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _

Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* *](-wia-iwiatransfercallback.md) вызывающего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

При скачивании папки также переносятся все дочерние элементы этой папки. Каждый элемент передается в отдельном потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 




