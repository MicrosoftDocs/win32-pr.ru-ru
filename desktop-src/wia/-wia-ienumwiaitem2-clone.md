---
description: Создает дополнительный экземпляр интерфейса IEnumWiaItem2 и отправляет обратный указатель на него.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Метод IEnumWiaItem2:: Clone (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810804"
---
# <a name="ienumwiaitem2clone-method"></a>Метод IEnumWiaItem2:: Clone

Создает дополнительный экземпляр интерфейса [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) и отправляет обратный указатель на него.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиенум* \[ заполняет\]
</dt> <dd>

Тип: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Получает адрес экземпляра интерфейса [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) , который создается **IEnumWiaItem2:: Clone** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенум* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
