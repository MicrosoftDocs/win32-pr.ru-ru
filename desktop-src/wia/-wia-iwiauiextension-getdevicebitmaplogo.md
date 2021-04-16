---
description: Возвращает пользовательский логотип точечного рисунка для устройства.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Метод Ивиауиекстенсион:: Жетдевицебитмаплого (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692422"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>Метод Ивиауиекстенсион:: Жетдевицебитмаплого

Возвращает пользовательский логотип точечного рисунка для устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает идентификатор устройства WIA, для которого должен быть получен значок.

</dd> <dt>

*фбитмап* \[ заполняет\]
</dt> <dd>

Тип: **хбитмап \** _

Указывает на место в памяти, которое будет принимать маркер эмблемы точечного рисунка для устройства.

</dd> <dt>

_nMaxWidth * \[ в\]
</dt> <dd>

Тип: **ulong**

Задает желаемую ширину точечного рисунка.

</dd> <dt>

*нмаксхеигхт* \[ окне\]
</dt> <dd>

Тип: **ulong**

Задает желаемую высоту точечного рисунка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl> |



 

 




