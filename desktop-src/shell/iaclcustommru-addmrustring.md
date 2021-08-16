---
description: Добавляет запись в список недавно использовавшихся (MRU).
title: 'Метод Иаклкустоммру:: Аддмрустринг'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: e5acd71a56ef0dd569315ee924313b10e27e6a4ba7ca75d1dbfa0d1e50932cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223598"
---
# <a name="iaclcustommruaddmrustring-method"></a>Метод Иаклкустоммру:: Аддмрустринг

Добавляет запись в список недавно использовавшихся (MRU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзентри* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на буфер, содержащий новую запись.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



 

 




