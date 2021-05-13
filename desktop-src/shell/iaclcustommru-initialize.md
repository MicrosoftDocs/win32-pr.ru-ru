---
description: Загружает список строк из реестра в список недавно использовавшихся (MRU).
title: 'Метод Иаклкустоммру:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841235"
---
# <a name="iaclcustommruinitialize-method"></a>Метод Иаклкустоммру:: Initialize

Загружает список строк из реестра в список недавно использовавшихся (MRU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзмрурегкэй* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на буфер, содержащий раздел реестра со строками для списка MRU.

</dd> <dt>

*двмакс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Максимальное число записей, которые могут быть взяты из *пвсзмрурегкэй*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



 

 




