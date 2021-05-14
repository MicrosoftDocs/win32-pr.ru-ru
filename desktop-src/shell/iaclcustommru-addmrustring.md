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
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842005"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



 

 




