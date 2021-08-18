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
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965853"
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

## <a name="remarks"></a>Remarks

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенум* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
