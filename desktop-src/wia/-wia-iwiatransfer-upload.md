---
description: Инициирует отправку данных одного элемента от вызывающего.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Метод Ивиатрансфер:: upload (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263131"
---
# <a name="iwiatransferupload-method"></a>Метод Ивиатрансфер:: upload

Инициирует отправку данных одного элемента от вызывающего.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
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

*псаурце* \[ окне\]
</dt> <dd>

Тип: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Указывает указатель на данные [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

_pIWiaTransferCallback * \[ в\]
</dt> <dd>

Тип: **[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _

Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* *](-wia-iwiatransfercallback.md) вызывающего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
