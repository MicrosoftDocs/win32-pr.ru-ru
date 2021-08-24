---
description: Возвращает количество элементов, хранящихся в этом перечислителе.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Метод IEnumWiaItem2:: NOCOUNT (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882424"
---
# <a name="ienumwiaitem2getcount-method"></a>Метод IEnumWiaItem2:: NOCOUNT

Возвращает количество элементов, хранящихся в этом перечислителе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*cElt* \[ заполняет\]
</dt> <dd>

Тип: **ulong \***

Получает указатель на **ulong** , которая получает количество элементов в перечислении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




